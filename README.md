# AutoTag
> Smart management of your music library - v1

## Table of contents
1. [Purpose](#purpose)
2. [Graphic User Interface (Windows)](#GUI)
3. [Command Line Interface (Linux & Windows)](#CLI)
4. [Next development](#next)
5. [Legal Notice](#notice)

## Purpose <a name="purpose"></a>

  Welcome ! This software has been developped to answer to one specific need : **to have a complete well-organized music library.**
  The user has two ways to use it, depending on which operating system he is using. He can use the Graphic Interface if he has a Windows   OS, or else the Command Line Interface.
  
  This software is composed of two main functions.
  1. Update the tags of the musics files
  2. Reorganize the music library
  
### 1. Update the tags of the music files
  The tags of a music file are the metadata of it. The ones handled by the software are the following :
* Album
* Artist
* Composer
* Disc
* Genre
* Title
* Track
* Year

Those metadata are often incomplete. We are using an API to fullfill or create the metadata from a sample of music. The next operation is to compare those new data with the previous one to be sure that there are no mistakes. Finally, we are rewriting the tags completed into the music file.

### 2. Reorganize the music library

Once the data are complete, we can now manage the library. The software allows the user to specify a target folder that can be as followed :
> C:\Users\Musics\\%Artist%\\%Album%\\%Track% - %Title%.mp3

The music files will be then renamed and moved (or copy) in the folder of their artists and the subfolder of their albums. For instance, if we have the music *Paradise* of *Coldplay*, it will be stored here :
> C:\Users\Musics\Coldplay\Mylo Xyloto\3 - Paradise.mp3


## Graphic User Interface <a name="GUI"></a>

To use AutoTag GUI on Windows, download the AutoTag/bin/GUI folder, and execute AutotagGUI.exe. The user will be asked to follow the previous steps described :
- Load a library from a folder,
- Update and write new tags,
- Reorganize the files by moving or copying them to another location with the previous method.


## Command Line Interface <a name="CLI"></a>

### Using in Linux

If the user wants to use AutoTag on Linux, he will need to use [Mono](http://www.mono-project.com/). 
After that he will be able to execute AutoTag (bin in AutoTag/bin/CLI)
> mono AutoTagCLI.exe [params]

For example (recognition of the music library and move to a new place):
> mono AutoTagCLI.exe -d /home/user/Music -dd /home/user/NewMusicFolder/%Artist%/%Title%.mp3 -rm

For some help about the usage of the CLI:
> mono AutoTagCLI.exe --help 

### Using in Windows

To use AutoTag CLI on Windows, download the AutoTag/bin/CLI folder, open a terminal in this folder.
Then you can use the CLI:
> AutoTagCLI.exe [params]

For some help about the usage of the CLI:
> AutoTagCLI.exe --help 

To use it from everywhere (and not only from the folder bin), just add AutoTagCLI.exe to your PATH.

## Next development <a name="next"></a>

Here is a non-exhaustive list of the next development that will be available soon:
* Manage other extensions than .mp3
* Propose a conversion to .mp3 to manage the tags
* Better comparison between the informations of the original file and the API
* Cross-case comparison with another database including the lyrics of the songs

## Legal Notice <a name="notice"></a>

The three authors of this software are :
* *Hachemin Pierre-Yves*
* *Seys Thibaut*
* *Vadot Antoine*


22/11/2017 : v1
