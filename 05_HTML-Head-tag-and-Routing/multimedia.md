# HTML Multimedia

## Table of Contents

1. [Introduction to Multimedia](#introduction-to-multimedia)  
2. [HTML Audio](#html-audio)  
3. [HTML Video](#html-video)  
4. [HTML Embed](#html-embed)  
5. [HTML Object](#html-object)  
6. [HTML Iframe](#html-iframe)  
7. [Conclusion](#conclusion)  


## Introduction to Multimedia

**Multimedia** in HTML refers to integrating different types of media, such as audio, video, images, or external content, into web pages. HTML provides tags to embed and control these media elements for a rich user experience.


## HTML Audio

The `<audio>` element is used to play sound files (e.g., music, recordings). It supports different audio formats like `MP3`, `WAV`, and `OGG`.

### Syntax

```html
<audio controls>
  <source src="audio-file.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

### Attributes:
- `controls` : Adds audio controls like play, pause, and volume.
- `autoplay` : Automatically starts playback when the page loads.
- `loop` : Repeats the audio after it ends.
- `muted` : Mutes the audio by default.

### Example:

```html
<h3>Audio Example</h3>
<audio controls loop>
  <source src="example-audio.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```


## HTML Video

The `<video>` element is used to embed video files. It supports formats like `MP4`, `WebM`, and `OGG`.

### Syntax

```html
<video width="400" controls>
  <source src="video-file.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

### Attributes:
- `controls` : Adds play, pause, and volume options.
- `autoplay` : Starts the video automatically.
- `loop` : Repeats the video.
- `muted` : Starts the video muted.
- `poster` : Displays an image before the video plays.

### Example:

```html
<h3>Video Example</h3>
<video width="400" controls poster="poster-image.jpg">
  <source src="example-video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```


## HTML Embed

The `<embed>` tag is used to embed external content like audio, video, or interactive media (e.g., PDFs or Flash).

### Syntax

```html
<embed src="example-file.mp4" width="400" height="300" type="video/mp4">
```

### Example:

```html
<h3>Embed Example</h3>
<embed src="example-video.mp4" width="400" height="300" type="video/mp4">
```


## HTML Object

The `<object>` tag embeds external resources like images, videos, and other multimedia, or even PDFs.

### Syntax

```html
<object data="file.pdf" type="application/pdf" width="600" height="400">
  Your browser does not support the object element.
</object>
```

### Example:

```html
<h3>Object Example</h3>
<object data="example.pdf" type="application/pdf" width="600" height="400">
  PDF file cannot be displayed.
</object>
```


## HTML Iframe

The `<iframe>` tag embeds another webpage or external content inside the current page.

### Syntax

```html
<iframe src="https://example.com" width="600" height="400" title="Iframe Example"></iframe>
```

### Attributes:
- `src` : Specifies the URL of the content to embed.
- `width` and `height` : Sets the size of the iframe.
- `title` : Provides an accessible name for the iframe.

### Example:

```html
<h3>Iframe Example</h3>
<iframe src="https://www.example.com" width="600" height="400" title="Embedded Website"></iframe>
```


## Conclusion

HTML provides powerful tags to integrate multimedia content, such as audio, video, and external media. By using tags like `<audio>`, `<video>`, `<embed>`, and `<iframe>`, developers can create dynamic and interactive web pages.