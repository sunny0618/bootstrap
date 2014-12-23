---
layout: page
title: Migrating to v4.x.x
---

## Summary

For a broader overview, see [what's new](http://blog.getbootstrap.com/DEAD-LINK-FIX-ME-PLEASE) in the v4.0.0 release announcement.

- Dropped IE8 support—v4 is now only IE9+. For sites needing IE8, use v3.
- Added official support for Android v5.0 Lollipop's Browser and WebView. Earlier versions of the Android Browser and WebView remain only unofficially supported.
- Switched from `px` to `rem` as our primary unit in CSS.
- Media queries are now in `em`s.
- Global font-size increased from `14px` to `16px`.
- Dropped panels, thumbnails, and wells for a new component, cards.
- Switched from LESS to SCSS for our source CSS files.
- Added a new grid tier for ~`480px` and below.
- Dropped Glyphicons icon font.
- Refactored nearly all components to use more unnested classes instead of children selectors.
- Non-responsive usage of Bootstrap is no longer supported.
- Dropped the online Customizer in favor of more extensive setup documentation.
- Replaced the separate optional theme with...

## Major class changes

This table shows the style changes between v3.x.x and v4.0.0.

| Bootstrap 3.x.x | Bootstrap 4.0.0 |
| --- | --- |
| Pager's `.previous` | `.pager-prev` |
| Pager's `.next` | `.pager-next` |
| Carousel's `.item` | `.carousel-item` |
| Tabs | |
| Pills | |
| Buttons | |

## What's new
We've added new components and changed some existing ones. Here are the new or updated styles.

| Component | Description |
| --- | --- |
| Cards | New, more flexible component to replace v3's panels, thumbnails, and wells. |
| New navbar | Replaces the previous navbar with a new, simpler component. |
| New progress bars | Replaces the old `.progress` `<div>` with a real `<progress>` element. |
| New table variants | |
| New utility classes | |

TODO: audit new classes that didn't exist in v3

## What's removed
The following components have been removed in v4.0.0.

| Component | Removed from 3.x.x | 4.0.0 Equivalent |
| --- | --- | --- |
| Panels |  | Cards |
| Thumbnails |  | Cards |
| Wells |  | Cards |
| Justified navs | | |

TODO: audit classes in v4 that aren't present in v4

The following deprecated Less/SCSS variables have been removed in v4.0.0:
* `@screen-phone`, `@screen-tablet`, `@screen-desktop`, `@screen-lg-desktop`. Use the more abstract `$screen-{xs,sm,md,lg,xl}-*` variables instead.
* `@screen-sm`, `@screen-md`, `@screen-lg`. Use the more clearly named `$screen-{xs,sm,md,lg,xl}-min` variables instead.
* `@screen-xs`, `@screen-xs-min`. The extra small breakpoint has no lower bound, so these variables were logically absurd. Reformulate your expression in terms of `$screen-xs-max` instead.
* `@grid-float-breakpoint`

TODO: audit list of stuff in v3 that was marked as deprecated

## Additional notes
- Removed support for styled nested tables (for now)