# finality 
768p :heavy_check_mark: 1080p :heavy_check_mark: 1440p :heavy_check_mark: 4k (150%) :heavy_check_mark: Mobile :heavy_check_mark: TV Mode :soon:

Jellyfin Theme CSS (Finishing TV mode, just waiting for logo support)

![g2](https://github.com/user-attachments/assets/6d9d0805-765a-4575-aee9-3a7c7cf26f6d)

For the black & white version, paste this into your Custom CSS Box

```css
@import url("https://cdn.jsdelivr.net/gh/tedhinklater/finality@main/finality.css");

```

or, import the colour version with

```css

@import url("https://cdn.jsdelivr.net/gh/tedhinklater/finality@main/Finality-Coloured.css");

```

<img src="https://github.com/user-attachments/assets/095e4d72-5132-4c65-b364-887337f97f2d" width="49.5%" height="49.5%" /> <img src="https://github.com/user-attachments/assets/a7b81d30-d30e-4eca-83e7-7111dd091466" width="49.5%" height="49.5%" /> 
<img src="https://github.com/user-attachments/assets/118a415c-96ab-4d43-a308-0e3ac4672f76" width="49.5%" height="49.5%" /> <img src="https://github.com/user-attachments/assets/9ca23383-801b-4f0c-8b0d-ee57759c7f33" width="49.5%" height="49.5%" />
<img src="https://github.com/user-attachments/assets/177a94d5-0f0b-40f4-9d1e-c5c59bcaabc3" width="49.5%" height="49.5%" /> <img src="https://github.com/user-attachments/assets/81d7d0eb-78b3-48e3-a81c-93f02a0e8d08" width="49.5%" height="49.5%" /> 

# Player 
![14](https://github.com/tedhinklater/finality/assets/66086488/84d70061-5216-4921-bff0-fbb25de59cca)

# Mobile
![mobile](https://github.com/tedhinklater/finality/assets/66086488/a0fb2aec-2794-4d68-b96c-9a144844729a)

Under "Display" make sure you enable backdrops and use the Dark theme

![darkbackdrops](https://github.com/user-attachments/assets/b69b1143-22c1-48df-b8e5-5aaa1869a97f)

# Optional Mods & Customization

## [Featured Content Bar](https://github.com/BobHasNoSoul/jellyfin-mods/blob/main/10.9.x.md#featured-content-bar-109xx) by [BobHasNoSoul](https://github.com/BobHasNoSoul) and [SethBacon](https://forum.jellyfin.org/u-sethbacon)

![featured](https://github.com/user-attachments/assets/c214cc03-9240-40c9-b7e1-9c3dc0634606)

1. Download [slideshow.html](https://github.com/tedhinklater/finality/blob/main/slideshow.html)

2. Enter your ```UserId``` into line 11 of slideshow.html (Get your UserID by going to the Jellyfin Dashboard, go to the Users tab, click your username. Your UserId is the last string in the address bar after the = sign)

3. Enter your ```API key``` into line 12 of slideshow.html (Go to Dashboard, API Keys tab, click the + and create a key for FeaturedSlideshow)

4. Go to your ```jellyfin-web``` folder (C:\Program Files\Jellyfin\Server\jellyfin-web) and create a folder named ```avatars``` and drop ```slideshow.html``` in that folder

5. (Important: Open Notepad with Administrator rights, or use Notepad++ for this) In the jellyfin-web folder, open the file ```home-html.RANDOMSTRINGHERE.chunk.js```

6. Ctrl+F and search for ```data-backdroptype="movie,series,book">``` 

7. Paste this after the >

```html
<style>.featurediframe { width: 89vw; height: 300px; display: block; border: 1px solid #000; margin: 0 auto}</style> <iframe class="featurediframe" src="/web/avatars/slideshow.html"></iframe>
```
8. Save the file.

9. Add this to your Custom CSS box in the Dashboard

```css
@import url("https://cdn.jsdelivr.net/gh/tedhinklater/finality@main/slideshow.css");
```

10. Empty your browser's cached web content (Ctrl+F5 or empty it from your browser's Cookies and Site Data settings section)

That's it.

## Changing your Jellyfin logo --> <img src="https://i.imgur.com/5d4W3M2.png" width="10%" height="10%"  /> 

Go into your Jellyfin server's Custom CSS and insert this (changing the obvious part):

```css
/*Use your own header logo*/
.pageTitleWithDefaultLogo {
  background-image: url(LOGO-URL-HERE);
}
```

## Scrolling Backdrop

```css
@import url("https://cdn.jsdelivr.net/gh/tedhinklater/finality@main/scrolling%20backdrop.css");

```

## ![Custom logo on login page](https://github.com/BobHasNoSoul/jellyfin-mods/blob/main/10.9.x.md#adding-your-logo-at-the-top-of-the-login-page-109x)

![login logo](https://github.com/user-attachments/assets/2f102c41-0632-402f-8c65-0b15eb9bb3c9)

