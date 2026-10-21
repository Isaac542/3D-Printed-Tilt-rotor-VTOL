# 3D printed tiltrotor VTOL

Single-page static site for GitHub Pages. No build step, no Jekyll.

## Structure

    index.html          the whole site (tiltrotor VTOL project page)
    assets/css/style.css
    assets/js/main.js
    media/              photos and video used on the page
    .nojekyll           tells GitHub Pages to serve files as-is

## Publish
1. Push everything in this folder (including the hidden `.nojekyll` file) to the repo root.
2. Repo Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.

## Adding or swapping photos and videos
Drop a file into `media/` and point a slot at it:

    <figure class="media" data-type="image"
            data-src="media/fuselage.jpg"
            data-alt="What the photo shows"
            data-caption="Caption under the photo."></figure>

- `data-type`: `image`, `video` (mp4), or `youtube`
- `data-src`: file path, or the YouTube video ID (the part after `v=`)
- `data-ratio`: placeholder shape, e.g. `16/9` (default), `4/3`, `1/1`
- add `data-loop` to a video to autoplay muted on loop

File names are case-sensitive on GitHub Pages: `photo.JPG` and `photo.jpg` are different files.
Export photos around 2000 px wide as JPG (~300 KB). GitHub rejects files over 100 MB, so
compress videos to 1080p H.264 mp4, or upload to YouTube and use `data-type="youtube"`.
