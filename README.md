# aframe-animation-toggle-component
An aframe component that toggles animations

![Multisrc component animated demo](https://github.com/elbobo/aframe-animation-toggle-component/blob/master/toggle_light.gif?raw=true)

# What?

A simple component that flips the direction on completion of the animation, so you only need to specify one animation then each time it is triggered it will play in the opposite direction to its previous cycle.

# How?

Just include the script in your header then using the `animation-toggle` attribute, add the list of animation names that you want to toggle on each run. 

```html
  <head>
    <script src="https://aframe.io/releases/0.9.1/aframe.min.js"></script>
    <script src="https://rawcdn.githack.com/elbobo/aframe-animation-toggle-component/7ef92afbc8b16ad34c1689945ff9f46c570be2d6/dist/aframe-animation-toggle-component.js"></script>
  </head>
  <body>
    <a-scene>
      
       <a-box
        id="box"
        position="0 1.6 -2"
        color="#333"
        rotation="0 45 0"
        animation__position="property: position; from: 0 1.6 -2; to: 0 1 -2; dir: alternate; startEvents: click"
        animation__color="property: color; from: #333; to: #ff0000; startEvents: click"
        animation__rotation="property: rotation; from: 0 45 0; to: 0 135 0; startEvents: click"
        animation-toggle="names: animation__position, animation__color, animation__rotation">
      </a-box>
      
    </a-scene>
  </body>
```

# API

Property | Description | Default
--- | --- | ---
names | Comma separated list of animation names | []



