bezier-spline-js
================

#Bezier Splines in Javascript.


Library for generating smooth curves passing through given points.

You know, when you need to move an object along a curve.

Usage:

	var spline = new Spline({
		points: array_of_control_points,
		duration: time_in_miliseconds,
		sharpness: how_curvy,
		stepLength: distance_between_points_to_cache
	});

	//generate the curve
	var spline = new Spline({
		points:[
		{x:130, y:130},
		{x:250, y:30},
		{x:400, y:200},
		{x:50, y:320},
		{x:100, y:500},
		{x:300, y:600},
		{x:600, y:530},
		{x:480, y:300},
		{x:500, y:100},
		{x:700, y:50},
		{x:850, y:320},
		{x:600, y:600},
		{x:350, y:520},
		{x:300, y:400}],
		duration:15000
	});

	// get the canvas context (assuming <canvas id="canvas"></canvas>)

	var canvas = document.getElementById("canvas");
	var ctx = canvas.getContext("2d");

	// draw: 

	spline.draw(ctx);

