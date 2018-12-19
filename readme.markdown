# CSS Less templating

This is a small POC to demonstrate a way to use themes with Less. 

`light-theme.html` and `dark-theme.html` each use their respective `light-theme.css` and `dark-theme.css` file. They're both inserted into `index.html` via iframes.

The Dark Theme uses dark colors but is otherwise as default, while the Light Theme uses light colors, as well as overwrite some text styling.

![CSS Less templating](screely.png "CSS Less templating")

`dark-theme.css`:
```css
/* /less/index.less */
html,
body {
  height: 100%;
}
body {
  background: black;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  overflow: hidden;
}
/* /less/components/_App.less */
.App {
  font-size: 4vw;
  letter-spacing: 5vw;
  color: white;
  text-transform: uppercase;
}
```

`light-theme.css`:
```css
/* /less/index.less */
html,
body {
  height: 100%;
}
body {
  background: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  overflow: hidden;
}
/* /less/components/_App.less */
.App {
  font-size: 4vw;
  letter-spacing: 5vw;
  color: black;
  text-transform: uppercase;
}
/* /less/secondary/components-overwrite/_App.less */
.App {
  font-size: 15vw;
  letter-spacing: -0.5vw;
  text-transform: none;
  transform: rotate(0.5turn);
}
```
