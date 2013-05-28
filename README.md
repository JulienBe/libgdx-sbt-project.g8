# libgdx sbt project

Configure and generate a Scala project for [libgdx](http://libgdx.badlogicgames.com/) using [g8](http://github.com/n8han/giter8) and [sbt](https://github.com/sbt/sbt) 0.12.

## Setting up a new project

To use this template, you will need to install g8 first.
Consult g8's [readme](http://github.com/n8han/giter8#readme) for more information.

Then, in your favorite shell, type the command:

    $ g8 ajhager/libgdx-sbt-project

After filling in some information about your project, you can start placing your game's source files and assets in common/src/main/scala and common/src/main/resources, respectively.

## Managing your project

Update to the lastest libgdx nightlies (You will need to do this at least once):

    $ sbt update-gdx 

Run the desktop project:

    $ sbt "project desktop" run

Run the android project on a device:
  
    $ sbt android:start-device

Visit [android-plugin](https://github.com/jberkel/android-plugin) for a more in-depth guide to android configuration and usage.

## iOS Support (not currently working)

Open the ios solution in Xamarin Studio and build.

Every time you make changes to your scala files, you will need to clean and build since Xamarin cannot pick up changes to files it does not track.

## Using with Intellij

Make sure you have Intellij 12 and the latest Scala plugin, then type:

    $ sbt "project common" gen-idea

You can now open the project, then create an "Android Application" build config using the android module and an "Application" build config using the desktop module.
