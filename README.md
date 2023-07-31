# youtube-popout-overlay
A simple CSS snippet for the YouTube popout live chat to make it into an OBS Studio overlay

## Snippets
### Baseline

```css
/* Variables */
:root {
  --obs-background: rgba(0, 0, 0, 0.25);
}

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


/* Background color */
html {
  --yt-spec-base-background: var(--obs-background)!important;
}
```


### Padding
```css
```
