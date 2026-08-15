Project 17: Background Images

1. background-image — Add an Image Behind Content
css
.hero {
  background-image: url('images/hero.jpg');
}

/* You can also use a full URL */
.hero {
  background-image: url('https://example.com/photo.jpg');
}
Important rules:
The path in url() is relative to your CSS file location
Always provide a background-color fallback in case the image fails to load
Background images sit behind the content — text on top is still readable
css
.hero {
  background-image: url('hero.jpg');
  background-color: #333333; /* fallback color */
}
2. background-size — How Big the Image Should Be
css
/* Original size — may be too small or too big */
.original {
  background-size: auto;
}

/* Stretch to fill both width and height — may distort */
.stretch {
  background-size: 100% 100%;
}

/* Cover — fills the entire box, cropping edges if needed */
.cover {
  background-size: cover;
}

/* Contain — shows the whole image, may leave empty space */
.contain {
  background-size: contain;
}

/* Fixed pixel or percentage values */
.custom {
  background-size: 500px 300px;
}
cover vs contain — the most important distinction:
cover = fills the box completely, some image gets cut off (best for hero sections)
contain = entire image is visible, box may have empty bars (best for logos)
3. background-position — Where the Image Sits
Controls which part of the image is visible, especially when using cover.
css
/* Keywords */
.top-left {
  background-position: left top;
}

.center {
  background-position: center center; /* or just 'center' */
}

.bottom-right {
  background-position: right bottom;
}

/* Percentages */
.custom {
  background-position: 20% 80%;
}

/* Pixels */
.precise {
  background-position: 50px 100px;
}
Default is left top — the top-left corner of the image aligns with the top-left corner of the box.
4. background-repeat — Prevent Tiling
By default, small images repeat like wallpaper. Stop that:
css
.no-repeat {
  background-repeat: no-repeat;
}

/* Or repeat in one direction only */
.repeat-x {
  background-repeat: repeat-x; /* horizontal only */
}
5. Shorthand — background
You can combine multiple properties:
css
.hero {
  background: #333 url('hero.jpg') no-repeat center/cover;
  /*        color   image        repeat  position/size */
}
Order: color image repeat position/size
6. background-attachment: fixed — Parallax Effect
The background stays still while content scrolls:
css
.parallax {
  background-image: url('mountains.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}