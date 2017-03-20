# Twenty-twenty
Slider View


Need to highlight the differences between two images? TwentyTwenty, a visual diff tool, makes it easy to spot them!

The Problem
We recently needed a way to showcase the visual differences between two images. Folks tend to typically place two images next to each other in hopes that it'll be clear exactly what changed. We even thought about having one image fade into another. But we knew there had to be an even better way to highlight the differences between two images. A way that would bring everything into focus.

One of our Design Leads pointed us to Canada Goose, a cold weather outfitter. They used a slider to highlight the differences between counterfeit material. It was exactly what we needed!

This sparked a few new ideas on how to do something similar for our own needs. It had to swipe between two images to show "before" and "after". Most of all, it had to be responsive. It had to work on all devices. Taking inspiration from Canada Goose's site, we came up with TwentyTwenty, a widget that is:

Responsive and functional on all devices
Doesn't require images to work
Works with Foundation out of the box


How it works
TwentyTwenty works by stacking two images on top of each other. As the slider moves across the image, it makes use of the CSS clip property to trim the image on the left. This allows the image on the right to show through the container.

We're using custom movement events from the jquery.event.move library in order to support 1:1 slider movement on mobile devices.\

How it works
TwentyTwenty works by stacking two images on top of each other. As the slider moves across the image, it makes use of the CSS clip property to trim the image on the left. This allows the image on the right to show through the container.


We're using custom movement events from the jquery.event.move library in order to support 1:1 slider movement on mobile devices.



It's easy to get started, just wrap two images inside of a container. The first image will be on the left and the second one will be on the right. Here's an example container:
<div id="container1">
  <img src="sample-before.png">
  <img src="sample-after.png">
</div>

Then call twentytwenty() on this container once the images have loaded:
$(window).load(function() {
  $("#container1").twentytwenty();
});



Preventing FOUC
If you'd like to prevent a FOUC, just add the twentytwenty-container class to your container like so:

<div id='container1' class='twentytwenty-container'>
  <img src='sample-before.png'>
  <img src='sample-after.png'>
</div>

