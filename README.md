# Boomerang 

Boomerang is a static Cydia repository that can be run on Github Pages using Jekyll, or anywhere else.

## About

Servers often aren't very cheap, and download bandwidth further raises the cost of Cydia repository servers. In order to counter this, Github Pages can be used to host a Cydia repository. Boomerang provides a very simple installation and update process, along with a modern Bootstrap design.

## Installation

### Node Generator
0. Install the node.js Boomerang generator with ```npm install boomerang-repo -g```
0. Run ```boomerang-init _directory_``` to generate a Boomerang repository.
0. If you are using Github Pages
  0. Create a Github Repository and add the remote
  0. In your new Boomerang directory:
    * Run ```git init```
    * Run ```git add -A``` to add all files
    * Run ```git commit -am "Initial Commit"```
    * Run ```git checkout -B gh-pages``` to checkout the web branch
    * Run ```git push -u origin gh-pages``` to push your changes


## Package JSON Files
* Packages are stored as ```<package>.json``` in the ```packages/``` directory. These files store all the relevant information about a package so that the website is able to retrieve it as users access depictions.

### Example Package File (InstaMute):
```json
{
	"name": "InstaMute",
	"package": "com.jake0oo0.instamute",
	"author": "Jake0oo0",
	"version": "1.0.1",
	"description": "Mute the more annoying users that you follow on Instagram from your main feed",
	"changelog": {
		"1.0.0": [
			"Initial Release"
		],
		"1.0.1": [
			"Fixed preference issue with 64bit devices"
		]
	},
	"screenshots": {
		"instamute1.jpg": "Mute users from their profile",
		"instamute2.jpg": "Edit muted users in the settings",
		"instamute3.jpg": "Unmute users from their profile"
	},
	"links": {
		"<span class=\"glyphicon glyphicon-heart\"></span> Developer's Twitter": "https://twitter.com/itsjake88"
	}
}
```

* ***Name:*** The name of the package that will be displayed as the title.
* ***Package:*** The full package of your .deb file that will be distributed.
* ***Author:*** The author's name or username, along with an email if wanted.
* ***Version:*** The current version o fthe application/tweak.
* ***Changelog:*** A hash of versions corresponding to an array of changes for the specific version. There should always be at least one version equal to the current version listed above.
* ***Screenshots:*** Once again, a hash of image file names that correspond to a caption or description for the image. Image paths are relative, and all images are stored in the ```images/``` directory.
* ***Links:*** Also a hash of HTML or text which corresponds to a link for the specified text. The key may be raw HTML if more content should be added, or it can be plain text. The URL can also be relative or an exact URL.

### Clone the example repository
0. You can find the example Boomerang repository at the repository [here](https://github.com/Jake0oo0/boomerang-example).
0. Clone the repository and change the remotes. You can now push your changes to your own repository.

## License
MIT

I would prefer that you leave at least one of the links to my [twitter](https://twitter.com/itsjake88) or to the boomerang repository in the depictions.

If you are using Boomerang for your repository, please shoot me an email, as I'd love to list it here!