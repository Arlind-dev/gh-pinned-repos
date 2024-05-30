# gh-pinned-repos

https://repos.sulej.ch/

**This is a fork of [egoist/gh-pinned-repos](https://github.com/egoist/gh-pinned-repos)**

## Changes

### Functional

```diff
- } from "https://deno.land/x/cheerio@1.0.4/mod.ts";
+ } from "https://deno.land/x/cheerio@1.0.7/mod.ts";
```

```diff
- const pinned = $(".pinned-item-list-item.public").toArray();
+ const pinned = $(".pinned-item-list-item").toArray();
```

```diff
- const stars = getStars($, item);
+ const stars = parseInt(getStars($, item));
```

```diff
- const stars = parseInt(getStars($, item));
+ const stars = getStars($, item);
```

```diff
- return $(item).find('a[href$="/stargazers"]').text().trim();
+ return parseInt($(item).find('a[href$="/stargazers"]').text().trim());
```

```diff
- return $(item).find('a[href$="/network/members"]').text().trim();
+ return parseInt($(item).find('a[href$="/forks"]').text().trim());
```

### Non-functional

```diff
-     <head>
-       <meta charset="utf-8" />
-       <title>GitHub pinned repos API</title>
-     </head>
-     <style>body {font-family: Helvetica, serif;margin: 30px;}</style>
-     <p>GET /?username=GITHUB_USERNAME</p>
-     <p>
-       <form action="/">
-         <input type="text" name="username" placeholder="username" />
-         <button type="submit">Go!</button>
-       </form>
-     </p>
-     <p>made by <a href="https://github.com/egoist">@egoist</a> · <a href="https://github.com/egoist/gh-pinned-repos">source code</a></p>
-   `,
+      <head>
+        <meta charset="utf-8" />
+        <title>GitHub pinned repos API</title>
+      </head>
+      <style>body {font-family: Helvetica, serif;margin: 30px;}</style>
+      <p>GET /?username=GITHUB_USERNAME</p>
+      <p>
+        <form action="/">
+          <input type="text" name="username" placeholder="username" />
+          <button type="submit">Go!</button>
+        </form>
+      </p>
+      <p>made by <a href="https://github.com/egoist">@egoist</a> · <a href="https://github.com/egoist/gh-pinned-repos">source code</a></p>
+      <p>forked by <a href="https://github.com/Arlind-dev/">@arlind-dev</a> · <a href="https://github.com/Arlind-dev/gh-pinned-repos">source code</a></p>
+    `,
```

And some format changes.
