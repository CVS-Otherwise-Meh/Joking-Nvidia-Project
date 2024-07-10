# The Jokingly Unfunny Nano Project

 Dad jokes are not cool. At least, to m,ost people they aren't. However, I think a dad joke would be pretty joke if it _wasn't_ from a dad. But where would it be funny from? A machine, obviously. Therefore, I had the notion that if I trained a nano to understand some bad jokes I printed out, people would actually laugh: seeing these jokes in a new light. So, here, we have some very silly dad jokes - really only 4 - that the people using this might get a chuckle out of.

![add image descrition here](direct image link here)

## The Algorithm + How To Run

The Nvidia Nano is a machine-learning type AI program that is well known for acting as a great intro to learning the basics of artificial intellegence. In this case, AI is used to recognize images. As humans, we can recognize images pretty easily - but AI has to learn like a baby with absolutely nothing in thier brain. In a project like this, we feed some images to our AI and have it see if it can read the images. In my case, only a couple hundred images were fed, but it doesn't mean it doesn't work well!

Nvidia's brain in learning this project worked (and works!) like this:

- 1. Images are taken and nested in the `nvidia/jetson-inference/python/training/classification/data`, and put inside it's own project folder in that.
  2. In the project folder made in there, 4 different objects are created in there. 3 are folders - named `test`, `train`, and `val` are created. The 4th object is a text file called "labels."
  3. In each of the three folders, different named folders for each object in the training are created. If we did object recognition of some tools, let's say, we'd have the folders `hammer`, `pliers`, and `saw` in each of the initial three folders. You'd put these names in the labels file like this: (insert image)
  4. The three folders inside each are where the machine will pick out images to be tested! While the `test` and `val` folders should each get about 10% of all images for each object, around 80% of the images that will be trained on should be in the` train` folder. This is because that is what the algorithm will read.
  5. Now that that is set up, we need to train the images! The nano should have a docker installed. If it is not, it is recommended to read this guide to get it installed. The commands should be run in the nvidia terminal. Guide is here -> https://gist.github.com/RodrigoCMoraes/c559954926f70df43ee9c396ef82668c
  6. To get in the docker, go into the terminal and go into the `jetson-inference` folder. There, write the command `./docker/run.sh` and you should be there!
  7. Now, head into the same file path as where your project folders are stored. Write the words `python3 train.py --model-dir=models/yourprojectname data/yourprojectname` in the terminal. This is what initializes the training process!
  8. So what is happening in the background as these epochs are running?
     - 1. Each image in test is being evaluated on how close the AI recognizes it.
       2. The image is tested against the val folder to see how much it recognizes it to each.
       3. The higher the recognition, the more it recognizes the val images to the other images and vice versa.
       4. The mroe you train, the higher chance it will both identify the image correctly snd the closer to 100% it will be!
          Super sick, am I right?

## Running this project

So if you've seen the way to set it up and how the files run, the next steps should be easy!
   -Steps 1 to 7 should be followed and the epochs should be ran enough times where you feel comfortable. To run multiple epochs, you can add `--epochs=` the desired amount of epochs to the end of the command.
Have fun trying this! You can run a video, too, to see how well the AI recognizes the images shown in front of the camera.

[View a video explanation here](video link)
