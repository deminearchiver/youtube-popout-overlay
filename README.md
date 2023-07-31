# YouTube Popout Overlay
A simple **CSS snippet** for the **YouTube popout** live chat to make it into an OBS Studio overlay

## Usage


## Snippets
### Baseline

> **Warning** other snippets **require** the snippet below.

```css
/* Variables */
:root {
  /* Background color */
  --obs-background: rgba(0, 0, 0, 0.25);

  /* Message author */
  --obs-message-author-font-size: 13px;

  /* Message content */
  --obs-message-content-font-size: 13px;

  /* Message padding */
  --obs-message-padding-top: 4px;
  --obs-message-padding-right: 24px;
  --obs-message-padding-bottom: 4px;
  --obs-message-padding-left: 24px;
}

/* ADVANCED */

/* Remove interactive elements */
yt-live-chat-header-renderer,
yt-live-chat-viewer-engagement-message-renderer,
#reaction-control-panel-overlay,
#separator,
#toast-container,
#panel-pages {
  display: none!important;
}

/* Hide the scrollbar */
#item-scroller {
  overflow-y: hidden!important;
}
#item-offset {
  position: absolute;
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
