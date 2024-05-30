# gh-pinned-repos

**this is a fork of https://github.com/egoist/gh-pinned-repos**

## Changes

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

https://repos.sulej.ch/
