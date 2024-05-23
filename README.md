# Animated Overlay for Twitch Channel

Animated tip overlay created for [@bernardin_gameplay](https://twitch.tv/bernardin_gameplay/)'s Twitch Channel, based on StreamElements custom CSS format.

<img src="./public/screenshot.png" alt="Screenshot" width="400px"/>

---

## How to add it to StreamElements?

- Log in
- On dashboard, select `Streaming tools` and then `Overlays`
- Create a `NEW OVERLAY` or, if you rather edit an old one, find its card and click on `EDIT`

### New Overlay

- Choose a resolution (1080p recommended) and click on `START`
- On dashboard, click on `ADD WIDGET`, then `ALERTS` and `AlertBox`
- Unmark every checkbox but `Tip alert`, then click on the cog ⚙ by its side
- Click on `SET IMAGE` and upload `dinheirinho.png` from our local **assets folder**
- Then click on `UPLOAD SOUND` and upload `obrigado.mp3` from our local **assets folder**
- Scroll to `Enable custom CSS` and activate it, then click on `OPEN CSS EDITOR`
- Replace the **HTML tab** values with our `container div` element. You can get it from `index.html` file, but you can copy it from here:

```html
<div id="container">
    <img src="{{image}}" alt="dinheirinho">
    <div>
        <p id="obrigado">
            <span id="span-1" class="color3">Obri</span><span id="span-2" class="color4">gado!</span>
        </p>
        <p id="pelo_dinheirinho">
            <span  id="span-3" class="color3">pelo</span>
            <span  id="span-4" class="color4">seu</span>
            <span  id="span-5" class="color3">dinhei</span><span id="span-6" class="color4">rinho</span>
        </p>
        <p id="valor">R${{amount}}</p>
    </div>
</div>
```

- Copy the whole content from our `style.css` file and paste it on **CSS tab**
- Delete all content from **JS tab** and **Fields tab** (as we used SASS locally, Fields will not be necessary)
- Finally, click on `Done`
- You're set!
- Feel free to add extra details to your overlay.



## Running locally?

Replace `{{image}}` and `{{amount}}` variables on body's HTML!

```html
<div id="container">
    <img src="./assets/dinheirinho.png" alt="dinheirinho">
    <div>
        <p id="obrigado">
            <span id="span-1" class="color3">Obri</span><span id="span-2" class="color4">gado!</span>
        </p>
        <p id="pelo_dinheirinho">
            <span  id="span-3" class="color3">pelo</span>
            <span  id="span-4" class="color4">seu</span>
            <span  id="span-5" class="color3">dinhei</span><span id="span-6" class="color4">rinho</span>
        </p>
        <p id="valor">R$1,00</p>
    </div>
</div>
```

## Using Sass?

Activate Sass Monitoring before updating `input.scss` file.

```bash
sass --watch ./sass/input.scss ./style.css
```