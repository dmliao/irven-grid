# Irven Grid #

Irven is a simple CSS grid framework that is very easy to customize through SCSS. All class names are variables, so it's easy to adapt the grid's classes to whatever you're already familiar with. The column layout, size, padding, separation, etc. are also all customizable.

The default layout uses a 12-column grid, like practically every other grid framework out there. Changing to a 16-column layout takes all of one variable change in SCSS. Want to make a 17 or 29-grid layout that folds down to mobile at 800px? Go nuts. (Please don't actually do that.)

Tested on Chrome, Firefox, and IE9+. I'm not too sure if it works on IE8.

## Getting Started ##

There are two CSS files provided: grid.css uses floats to render columns, grid-inline uses inline-block divs. Pick whichever one you like better, and just link to it from your head:

	<link rel="stylesheet" href="css/grid.css">

## Structuring Content ##

You can change the grid's class names to whatever, so we'll assume here that you're using the default names.

	<div class="frame">
		<div class="row">
			<div class="c-4">Content</div>
			<div class="c-4">Content</div>
			<div class="c-4">Content</div>
		</div>
	</div>

...creates a 3-column grid layout, assuming that you're sticking with the default 12-column total.

You can also mix and match different column widths, anything from 1 to the number of total columns:

	<div class="frame">
		<div class="row">
			<div class="c-8">Content</div>
			<div class="c-4">Content</div>
		</div>
	</div>

...creates a 2-column layout with the right sidebar 1/2 the width of the left main content.

If you're using grid.css (with floats), you'll need to wrap your columns in a row class to clear the floats. However, *grid-inline.css doesn't use need to use rows!* (However, if you don't, make sure that your column numbers add up so that the layout looks right.)

## Why did I make this? ##

I'll get started by saying that I love Bootstrap. I use it probably far too often, and for everything...but for very small, simple sites, it's a bit bloated. Even if I strip out everything except the CSS grid, there's still a lot of typography and basic styles that go into it.

So this project is nothing but a grid. No text styling, just grid.

I'm also way too used to Bootstrap's grid naming convention, and trying to update my old projects to use a new grid often involves me changing every single frame, column, row, to match the new grid's naming convention. So that's why when I decided to make Irven, I made all the names variables, so that they could be edited to the user's preference.

And with everything else I do, this is a learning experience most of all, which I'm just sharing. Use it, learn from it, create your own grid, go nuts.

## Todo ##

'Cause even the simplest things can still be worked on.

* Images, images, images. I'm not quite sure what to do with them yet, whether I should make them resize with the grid or not, but the grid has to be able to handle them more elegantly.