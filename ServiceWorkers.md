# Service Worker

JS File registered with browser. Huge requirements for web apps

With Service Worker
Web Browser > Service Worker > Remote Server

- Can't directly access the DOM
- Programmable network proxy
- Promises
- Requires HTTPS

# User

Use Cases

- Caching assets & API calls
- Push Notifications
- Background data sync/preload
- Used in PWA

Service Worker Lifeycle

Register > Install > Active

`fetch`, `push` and `sync`

`serviceWorker.js`

```js
// It is for indivudual file fetching
// Call Install Event
const cacheName = "v1";

const cacheAssets = [
  "index.html",
  "about.html",
  "/css/style.css",
  "/js/main.js"
];

self.addEventListener("install", e => {
  console.log("Service Worker installed");

  e.waitUntil(
    caches
      .open(cacheName)
      .then(cache => {
        console.log(`Service worker: Caching Files`);
        cache.addAll(cacheAssets);
      })
      .then(() => self.skipWaiting())
  // );
});

self.addEventListener("activate", e => {
  console.log("Service Worker activated");

  e.waitUntil(
    caches.keys().then(cacheNames => {
      cacheNaems.map(cache => {
        if (cache !== cacheName) {
          console.log("Service Worker: Clearing Old Cache");
          return caches.delete(cache);
        }
      });
    })
  );
});

// Call Fetch Event
```

```js
// Site fetching
const cacheName = "v1";

self.addEventListener("install", e => {
  console.log("Service Worker installed");
});

self.addEventListener("activate", e => {
  console.log("Service Worker activated");

  e.waitUntil(
    caches.keys().then(cacheNames => {
      cacheNaems.map(cache => {
        if (cache !== cacheName) {
          console.log("Service Worker: Clearing Old Cache");
          return caches.delete(cache);
        }
      });
    })
  );
});
self addEventListener('fetch', e => {
  console.log('Service Worker: Fetching');
  e.respondWith(
    fetch(e.request)
      .then(res => {
        // Make copy/clone of response
        const resClone = res.clone();
        // Open cache
        caches
          .open(cacheName)
          .then(cache => {
            // Add response to cache
            cache.put(e.request, resClone);
          });
          return res;
      }).catch(err => caches.match(e.request).then(res => res))
  )
})
```

`main.html`

```js
if (navigator && navigator.serviceWorker) {
  window.addEventListener("load", () => {
    navigator.serviceWorker
      .register("../sw_cached_pages.js")
      .then(reg => console.log("Service worker: Registered"))
      .catch(err => console.log(`Service worker: Error: ${error}`));
  });
}
```

## References

[MDN- Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)
