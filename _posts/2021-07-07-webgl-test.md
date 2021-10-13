---
title: "Graphic Project"
filename: 2021-07-07-webgl-test.md
categories:
  - WebGL
permalink: /posts/webgl
layout : posts
---

## Project Description

Solo graphic project using sdl, glew

## Date

June, 2019 - July, 2019

## Feature

- Tech
  - 3D Math & Transform
  - simple diffuse color
  - 3D Camera Movement
  - WebGL import with emscripten

## Demo
<div class=emscripten>
	<progress hidden id=progress max=100 value=0></progress>
</div>
<div class=emscripten_border>
	<canvas class="emscripten" id="canvas" height="640" width="360"></canvas>
</div>
<script>
	var progressElement=document.getElementById("progress"),
		Module=
		{
			preRun:[],
			postRun:[],
			print:function()
			{
				var e=document.getElementById("output");
				return e&&(e.value=""),
						function(t)
						{
							arguments.length>1&&(t=Array.prototype.slice.call(arguments).join(" ")),
							console.log(t),
							e&&(e.value+=t+"\n",e.scrollTop=e.scrollHeight)
						}
			}(),
			printErr:function(e)
			{
				arguments.length>1&&(e=Array.prototype.slice.call(arguments).join(" ")),
				console.error(e)
			},
			canvas:function()
			{
				var e=document.getElementById("canvas");
				return e.addEventListener("webglcontextlost",
					(function(e)
					{
						alert("WebGL context lost. You will need to reload the page."),e.preventDefault()
					}),
					!1),
					e
			}(),
			setStatus:function(e)
			{
				if(Module.setStatus.last||(Module.setStatus.last={time:Date.now(),text:""}),
				e!==Module.setStatus.last.text)
				{
					var t=e.match(/([^(]+)\((\d+(\.\d+)?)\/(\d+)\)/),
						n=Date.now();
						t&&n-Module.setStatus.last.time<30||(Module.setStatus.last.time=n,Module.setStatus.last.text=e,
						t?(e=t[1],progressElement.value=100*parseInt(t[2]),progressElement.max=100*parseInt(t[4]),
						progressElement.hidden=!1):(progressElement.value=null,progressElement.max=null,progressElement.hidden=!0))
				}
			},
			totalDependencies:0,monitorRunDependencies:function(e)
			{
				this.totalDependencies=Math.max(this.totalDependencies,e),
				Module.setStatus(e?"Preparing... ("+(this.totalDependencies-e)+"/"+this.totalDependencies+")":"All downloads complete.")
			}
		};
	window.onerror=function(e)
	{
		Module.setStatus=function(e)
		{
			e&&Module.printErr("[post-exception status] "+e)
		}
	}
</script>
<script async src="/assets/html/webgltest/cs250_project1.js"></script>

press space bar for change perspective