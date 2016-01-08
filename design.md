# Solve Dots

## Design Specification

The design specificaiton is a counterpart to the Functional Speciffication. Where a functional specification concerns itself
with inputs and outputs from the program, or the *experience* of a user running the program, the design specification is concerned with decisions that the engineer and programmer must make during its creation.

The design specification should include information like:

* What tools or frameworks will you use to build the project (e.g. http://runpython.com or ggame)?
* What language will you use for coding (usually Python 3)?
* For every element of the Functional Specification, what code will need to be written to support it?
* What data will be stored or manipulated by the program? How will it be encoded and organized?
* Describe the logic and/or code behind every interaction with the user, and behind everything displayed.
* If your program uses an unusual or notable *algorithm*, what is the algorithm and how does it work?



Solve Dots will use phongap(cordova) to run javascript on a mobile device. Phonegap also allows me to access device Apis like the photo library to retrieve a picture of the dots board. Once an image is selected, I convert it into a canvas element where I can check which colors the dots are. This data is sent as a string to a Ruby 2.2.1 Api on the planet message server through ajax. The Api returns a list of coordinates to the app for the best possible move. The coordinates are then shown to the user.

To make this program, I have to make a ruby Api that takes the grid as a parameter, and can find and return the best move based on those parameters.

It will not store any data.
