<div align="center">
  <h1>YouTube Chat Overlay</h1>
  <p>
    <a href="#usage"><b>CSS snippets</b></a> and <a href="#other"><b>other tools</b></a> for customizing the <b>YouTube Popout Chat</b>
  </p>
  <a href="https://obsproject.com/">
    <img alt="Made for OBS Studio" src="https://img.shields.io/badge/MADE_FOR-OBS_Studio-black?style=for-the-badge&logo=obsstudio">
  </a>
  <img alt="Requires Chromium" src="https://img.shields.io/badge/Requires-CSS3-blue?style=for-the-badge&logo=css3">
</div>




## Usage
## Troubleshooting
### Browser Source resize delay
[![Requires OBS Shaderfilter](https://img.shields.io/badge/Requires-OBS_Shaderfilter-white?logo=obsstudio)](https://github.com/exeldro/obs-shaderfilter/ "exeldro/obs-shaderfilter")

Since the Browser Source in OBS Studio run asyncronously in a separate process, it can't keep up with the Move Transition animations.

You can use OBS Shaderfilter to partly fix this issue.
> TODO: add custom shader (coming soon)


# LEGACY



## Snippets
### Baseline

> **Warning** other snippets **require** the snippet below.

```css
/* Variables */
:root {
  /* Background color */
  --obs-background: rgba(0, 0, 0, 0.25);

  /* Message author */
  --obs-message-author-font-size: 18px;

  /* Message content */
  --obs-message-content-font-size: 16px;

  /* Message padding */
  --obs-message-padding-top: 8px;
  --obs-message-padding-right: 16px;
  --obs-message-padding-bottom: 8px;
  --obs-message-padding-left: 16px;
}

/* ADVANCED */

/* Remove interactive elements */
yt-live-chat-header-renderer,
yt-live-chat-viewer-engagement-message-renderer,
#reaction-control-panel-overlay,
#separator,
#toast-container,
#panel-pages,
#action-panel {
  display: none!important;
}

/* Hide the scrollbar */
#item-scroller {
  overflow-y: hidden!important;
}
#item-offset {
  position: absolute!important;
  left: 0;
  bottom: 0;
  right: 0;
}

/* Background color */
html {
  --yt-spec-base-background: var(--obs-background)!important;
  --yt-live-chat-message-highlight-background-color: transparent!important;
}

/*  */
yt-live-chat-author-chip {
  font-size: var(--obs-message-author-font-size)!important;
}
#message {
  font-size: var(--obs-message-content-font-size)!important;
}

/* Message padding */
yt-live-chat-text-message-renderer {
  padding-top: var(--obs-message-padding-top);
  padding-right: var(--obs-message-padding-right);
  padding-bottom: var(--obs-message-padding-bottom);
  padding-left: var(--obs-message-padding-left);
}
```

### Avatars configuration
- Hide
```css
/* Hides avatars */
yt-img-shadow {
  display: none!important;
}
```
- Customize
```css
/* TBD */
```

### Usernames
#### Author Chip
```css
#author-name.yt-live-chat-author-chip {
  border-radius: 8px;
}
yt-live-chat-author-chip[is-highlighted] #author-name.yt-live-chat-author-chip {
  padding: 2px 12px;
}
```
