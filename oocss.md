# OOCSS
The OO part of this methodology is through producing reusable code. Not on instantiating "classes".

## Methodology
Separation of Structure from Skin

We're used to thinking with a certain direction. 
  1. Find the class/ID
  2. Manipulate that DOM element in it's entirety

### Before
```
#button {
  width: 200px;
  height: 50px;
  padding: 10px;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}

#box {
  width: 400px;
  overflow: hidden;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}

#widget {
  width: 500px;
  min-height: 200px;
  overflow: auto;
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}
```

OOCSS encourages us to think the other way around. (Similar to bootstrap mentality).
  1. Style structures and skins
  2. Apply those strcutres and skins onto your HTML

### After
```
.button {
  width: 200px;
  height: 50px;
}

.box {
  width: 400px;
  overflow: hidden;
}

.skin {
  border: solid 1px #ccc;
  background: linear-gradient(#ccc, #222);
  box-shadow: rgba(0, 0, 0, .5) 2px 2px 5px;
}

.globalwidth {
  width: 980px;
  margin: 0 auto;
  position: relative;
  padding-left: 20px;
  padding-right: 20px;
  overflow: hidden;
}
```

**Objects**
- container
- style

You would apply these "CSS Objects" onto the HTML elements.

### Example
```
<header>
  <div class="globalwidth">
  </div>
</header>

<div class="box skin">
</div>

<button class="button skin">Text</button>
```

## Benefits
- DRY
- Speed
- Organization
- IDs for Javascript
- maintaining stylesheets
- Powerful when paired with Sass
- The Media object, best styling for injecting medias

## Resources

**Intro to OOCSS**
https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/

**OOCSS + Sass**
http://thesassway.com/intermediate/using-object-oriented-css-with-sass

https://ianstormtaylor.com/oocss-plus-sass-is-the-best-way-to-css/

**Media Objects**
http://www.nicoespeon.com/en/2013/05/dive-into-oocss/


