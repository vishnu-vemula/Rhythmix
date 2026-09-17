# Background gallery

Hero backdrop images for the Rhythmix landing page.

| File             | Notes                                    |
| ---------------- | ---------------------------------------- |
| `bg-money-1.jpg` | **Active backdrop** (referenced by `--hero-bg` in `assets/css/styles.css`) |
| `bg-money-2.jpg` | Alternate backdrop                       |
| `bg-money-3.jpg` | Alternate backdrop                       |
| `bg-money-4.jpg` | Alternate backdrop                       |
| `bg-money-5.jpg` | Alternate backdrop                       |
| `bg-money-6.jpg` | Alternate backdrop                       |

## Switching the backdrop

1. Pick (or add) an image in this folder using the `bg-<name>.<ext>` naming
   convention — lowercase, hyphen-separated, `.jpg`/`.png`/`.webp`.
2. Update the `--hero-bg` token in `assets/css/styles.css`:

   ```css
   --hero-bg: url("../img/bg-money-3.jpg");
   ```

3. Prefer images at least **1920 × 1080** so they stay sharp on large
   displays. Optimize them (e.g. [Squoosh](https://squoosh.app)) before
   committing — keep each file under ~500 KB.
