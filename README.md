Pixi Renderer
=============

#### JavaScript 2D Renderer ####

The aim of this project is to provide a fast lightweight 2D library that works across all devices.
The Pixi renderer allows everyone to enjoy the power of hardware acceleration without prior knowledge of webGL.
Also its fast.

### Demo ###

[Check out the Bunny Demo here](http://matgroves.com/pixijs/)

### Current features ###

- webGL renderer (with automatic smart batching allowing for REALLY fast performance)
- canvas renderer
- full scene graph
- super easy to use API (similar to twhe flash display list API)
- support for texture atlas's
- asset loader / sprite sheet loader
- auto detect which renderer should be used

### Coming soon ###

- Filters
- Render Texture
- Text
- Interactivity
- Documentation


### Coming later ###

- Awesome Post processing effects

### Usage ###

```javascript
	
	/*
		you can use either PIXI.WebGLRenderer or PIXI.CanvasRenderer
	*/
	var renderer = new PIXI.WebGLRenderer(800, 600); 

	document.body.appendChild(renderer.view);
	
	var stage = new PIXI.Stage;

	var bunnyTexture = new PIXI.Texture.fromImage("bunny.png");
	var bunny = new PIXI.Sprite(bunnyTexture);
	
	bunny.position.x = 400;
	bunny.position.y = 300;
	
	bunny.scale.x = 2;
	bunny.scale.y = 2;
	
	stage.addChild(bunny);
	
	requestAnimationFrame( animate );
	
	function animate() {
		
		requestAnimationFrame( animate );
		
		bunny.rotation += 0.01;
		
		renderer.render(stage);
	}
```

This content is released under the (Link Goes Here) MIT License.


