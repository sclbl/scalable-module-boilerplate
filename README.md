# scalable-module-boilerplate

A starting point for Scalable modules. Includes the module base, skeleton and fontawesome.

* [Included Packages](#included-packages)
* [Installation](#installation)

## <a name="included-packages"></a> Included Packages

* [sclbl:module-base](https://github.com/sclbl/module-base/)
* [skeleton:skeleton](https://github.com/pmuens/skeleton/)
* [fortawesome:fontawesome](https://github.com/MeteorPackaging/Font-Awesome/)

## <a name="installation"></a> Installation

1. Clone this repo to `<your_module>`

  `git clone https://github.com/Sclbl/scalable-module-boilerplate.git <your_module>`

2. Remove `.git`

  `cd <your_module> && rm -rf .git`

3. Update `settings.json`

  Replace `<Module Name>`, `<Developer Name>` and `"rootUrl": "http://host:port"` with your information.

  Example: The Scalable Notes module with Scalable core running locally on port 3000 and secretKey XXX.

	```
	{
	  "public": {
	    "scalable": {
	      "module": {
	        "name": "Notes",
	        "developer": "Scalable"
	      },
	      "core": {
	        "settings": {
	          "rootUrl": "http://127.0.0.1:3000"
	        }
	      }
	    }
	  },
	  "scalable": {
	    "core": {
	      "settings": {
	        "secretKey": "XXX"
	      }
	    }
	  }
	}
	```

4. Run Scalable core locally on port 3000 with

  `meteor --settings settings.json --port 3000`

5. Run your module locally on a free port with your settings

  e.g. `meteor --settings settings.json --port 4000`

  The module will automatically register itself and should be visible seconds after that.

6. Happy coding!
