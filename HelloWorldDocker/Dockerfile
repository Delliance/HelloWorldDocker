# This is the image for java 17, you cna remove the :17 so it automatically uses the latest version
FROM openjdk:17

# Copy the app files from host machine to image filesystem
# the first argument is what I want to copy, the second "/src" is where it'll be copied, here I just named it the same
# COPY the first argument applies to my host machine, the second to the image
COPY src /src

# Create a new app directory for my application files, this will create a directory that lives inside the container not
# the host machine
# RUN only applies to images
RUN javac src/com/danieltesting/testingdocker/Main.java

# javac is for .java-----java is for compiled so .class

# Set the directory for executing future commands, I don't know how to use this shit, no matter what I place here in
# WORKDIR it always make that when I run the image an exception of classnotfound appears
# WORKDIR src /src

# This is the command that will be executed when you run the container from the image
# ALL DOCKER files must include one command or entry point with instructions specifying the default instruction for the
# container:
# Run the Main Class
CMD java -classpath src com.danieltesting.testingdocker.Main

# These instructions basically say this: pull and copy JDK image, copy my application files into the image and run the
# application when the container starts




#################### All of this can be ran with the start icon on IntelliJ but if does not appear, use the terminal:

######## docker build -t hello-world:1.0 .


# hello-world is the image name
# :1.0 is a tag for the version, not necessary
# last you need to specify where the docker file is located, normally when you're in the terminal, you're already in the
# location so you can just place a point at the end "."

######################33 To see all the images you currently have in the terminal:

# docker images

################### To  actually run the container us the next command in the terminal:

# docker run hello-world:1.0           as you can see just say docker to run the name of the app with the tag

########################### You can see all the containers and images opening docker app but you can also delete or
# check the containers in the terminal as:

# to delete image:    docker rmi IdOfTheImage
# to see containers:    docker ps            this one only shows running containers
# tp see ALL containers  docker ps -a

###########################3 you can run the app in the background, meaning that nothing will appear in the console

# docker run -d hello-world:1.0

# of you run in the bakcground, you can check the logs in the docker app, or in the console with;

# docker logs IdOfTheImage

###################################### you can stop the conainer from the docker app