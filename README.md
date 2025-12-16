# Redirector

Browser extension (Chrome, Vivaldi, Edge) to redirect URLs based on regex or wildcard patterns.

## Installation

Load as an unpacked extension:
1. Go to `chrome://extensions`
2. Enable "Developer mode"
3. Click "Load unpacked"
4. Select this directory

## Examples

### De-mobilizer
- Example URL: `https://en.m.wikipedia.org/`
- Include pattern: `^(https?://)([a-z0-9-]*\.)m(?:obile)?\.(.*)`
- Redirect to: `$1$2$3`
- Pattern type: Regular Expression
- Description: Always show the desktop version of websites

### AMP redirect
- Example URL: `https://www.google.com/amp/www.example.com/amp/document`
- Include pattern: `^(?:https?://)www.(?:google|bing).com/amp/(?:s/)?(.*)`
- Redirect to: `https://$1`
- Pattern type: Regular Expression

### YouTube Shorts to YouTube
- Example URL: `https://www.youtube.com/shorts/video-id`
- Include pattern: `^(?:https?://)(?:www.)?youtube.com/shorts/([a-zA-Z0-9_-]+)(.*)`
- Redirect to: `https://www.youtube.com/watch?v=$1$2`
- Pattern type: Regular Expression
- Advanced option: enable `historyState`

### Doubleclick escaper
- Example URL: `https://ad.doubleclick.net/ddm/trackclk/N135005.2681608PRIVATENETWORK/B20244?https://www.example.com`
- Include pattern: `^(?:https?://)ad.doubleclick.net/.*\?(http?s://.*)`
- Redirect to: `$1`
- Pattern type: Regular Expression

## License

MIT
