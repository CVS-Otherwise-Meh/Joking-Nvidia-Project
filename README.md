# The Jokingly Unfunny Nano Project

 Dad jokes are not cool. At least, to m,ost people they aren't. However, I think a dad joke would be pretty joke if it _wasn't_ from a dad. But where would it be funny from? A machine, obviously. Therefore, I had the notion that if I trained a nano to understand some bad jokes I printed out, people would actually laugh: seeing these jokes in a new light. So, here, we have some very silly dad jokes - really only 4 - that the people using this might get a chuckle out of.

![add image descrition here](direct image link here)

## The Algorithm

The Nvidia Nano is a machine-learning type AI program that is well known for acting as a great intro to learning the basics of artificial intellegence. In this case, AI is used to recognize images. As humans, we can recognize images pretty easily - but AI has to learn like a baby with absolutely nothing in thier brain. In a project like this, we feed some images to our AI and have it see if it can read the images. In my case, only a couple hundred images were fed, but it doesn't mean it doesn't work well!

Nvidia's brain in learning this project worked (and works!) like this:

- 1. Images are taken and nested in the `nvidia/jetson-inference/python/training/classification/data`, and put inside it's own project folder in that.
  2. In the project folder made in there, 4 different objects are created in there. 3 are folders - named `test`, `train`, and `val` are created. The 4th object is a text file called "labels."
  3. In each of the three folders, different named folders for each object in the training are created. If we did object recognition of some tools, let's say, we'd have the folders `hammer`, `pliers`, and `saw` in each of the initial three folders. You'd put these names in the labels file like this: (insert image)
  4. The three folders inside each are where the machine will pick out images to be tested! While the `test` and `val` folders should each get about 10% of all images for each object, around 80% of the images that will be trained on should be in the` train` folder. This is because that is what the algorithm will read.
  5. Now that that is set up, we need to train the images! The nano should have a docker installed. If it is not, it is recommended to read this guide to get it installed. The commands should be run in the nvidia terminal. Guide is here -> https://gist.github.com/RodrigoCMoraes/c559954926f70df43ee9c396ef82668c
  6. To get in the docker

## Running this project

1. Add steps for running this project.
2. Make sure to include any required libraries that need to be installed for your project to run.

[View a video explanation here](video link)
