# Smart Mirror Project
My project is the Smart Mirror using the magic mirror software to show many applications called modules each having different functions. Through these few weeks I was able to learn how to install many modules onto mirrors and how to edit them through css and java script. My smart mirror can display basic modules like my calendar and weather and more interesting modules like being able to display a large spinning globe, show interactive chess puzzles, and display the music I listen to on spotify in real time while also being a reflective mirror..

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Bill W. | International Community School | Software Engineering | Incoming Sophmore

![IMG_6159](https://github.com/user-attachments/assets/64cf19a1-9644-45d1-b18e-e2f368937b1c)

)
  


# Second Milestone



<iframe width="560" height="315" src="https://www.youtube.com/embed/pFjmpbU6Lu8?si=69HFv4WDD_iIQSxV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

So far for milestone two I changed to a larger display to show the smart mirror, and I added a film and many more modules to the mirror. The film I added to the display is reflective so that the display can reflect objects and people like a mirror. The film was pretty difficult to put onto the mirror because it was larger than the display and I had to carefully cut the film so that it was the correct size. I tried my best to put the film on perfectly but I could never put the film onto the display with no air bubbles. At the end I just did the best I could and I was able to successfully have a reflective display that just had a few air bubbles.


After putting on film it was most reflective when the background was pitch black and when I had my background module on it made the film nearly useless. Another problem that arose was through the long list of modules on github there were many that I wanted to add and my magic mirror display was getting too cramped to fit more modules. After some searching I came across a page module that allowed me to create many different pages on my smart mirror. The page module also recommended an indicator module to navigate between the pages. After adding both of these modules I was able to continue adding more modules and in addition fix my reflective film problem by dedicating a page to show my reflective film. I added a movie info module on the first page which shows popular movies. On the second page I only added a globe module which shows a pretty large spinning globe. On the third page I added a textclock module to have a different way to tell the time, a quote module that specifically showed stoic quotes, a puzzle module that shows different chess puzzles that I can solve, I also added a planet rise module to shows the rise and set times of planets relative to my time, and I added a nasa astronomy image module that changes the astronomy image daily as my background. On the fourth page I have it as pitch black so that the film on my mirror can be most reflective.

On my previous milestone it was still pretty difficult to add modules due to the many long files and problems such as modules being too large or overlapping other applications. But by adding more modules I face these problems a lot more and through learning and practice I was able to figure out solutions easily and I am comfortably able to add more modules.

I still wish to add voice activation so that I can navigate through my pages using my voice instead of my mouse and computer. I also still want to add a camera so that the mirror can understand my motions such as waving or getting distracted and can send me a warning or a signal to respond to my actions.

# First Milestone



<iframe width="560" height="315" src="https://www.youtube.com/embed/vAhzwOk_3u8?si=VIA64c6HJX5M6EU7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


My project is the Smart Mirror, which uses an open source modular smart mirror platform called Magic Mirror. The Smart Mirror is powered by raspberry pi and is displayed on a HDMI monitor. So far I have finished the basis of the smart mirror and added and changed a few modules. I added a spotify module which is connected to my spotify account as well as a background module that allows me to put different background images on my Smart Mirror. I also modified the size and the place of certain modules on the mirror so that all the modules are displayed normally. 

A few challenges I have been finding are learning different commands to add modules and changing the placement of certain modules. Adding modules requires me to put certain commands into the raspberry pi terminal which I have never done before, and modifying modules was difficult as each module has many files in different coding languages such as CSS and Javascript that affect module placement and function.

I hope to implement a few more modules onto my smart mirror to improve the variety of functions my smart mirror can display. I'm also interested in adding a camera to the mirror or speakers and microphone so that I can code the Smart Mirror to react to certain sounds or movements.



# Code


```c++
/* Config Sample
 *
 * For more information on how you can configure this file
 * see https://docs.magicmirror.builders/configuration/introduction.html
 * and https://docs.magicmirror.builders/modules/configuration.html
 *
 * You can use environment variables using a `config.js.template` file instead of `config.js`
 * which will be converted to `config.js` while starting. For more information
 * see https://docs.magicmirror.builders/configuration/introduction.html#enviromnent-variables
 */

    

let config = {
	


	
	address: "localhost",	// Address to listen on, can be:
							// - "localhost", "127.0.0.1", "::1" to listen on loopback interface
							// - another specific IPv4/6 to listen on a specific interface
							// - "0.0.0.0", "::" to listen on any interface
							// Default, when address config is left out or empty, is "localhost"
	port: 8080,
	basePath: "/",	// The URL path where MagicMirror² is hosted. If you are using a Reverse proxy
									// you must set the sub path here. basePath must end with a /
	ipWhitelist: ["127.0.0.1", "::ffff:127.0.0.1", "::1"],	// Set [] to allow all IP addresses
									// or add a specific IPv4 of 192.168.1.5 :
									// ["127.0.0.1", "::ffff:127.0.0.1", "::1", "::ffff:192.168.1.5"],
									// or IPv4 range of 192.168.3.0 --> 192.168.3.15 use CIDR format :
									// ["127.0.0.1", "::ffff:127.0.0.1", "::1", "::ffff:192.168.3.0/28"],

	useHttps: false,			// Support HTTPS or not, default "false" will use HTTP
	httpsPrivateKey: "",	// HTTPS private key path, only require when useHttps is true
	httpsCertificate: "",	// HTTPS Certificate path, only require when useHttps is true

	language: "en",
	locale: "en-US",
	logLevel: ["INFO", "LOG", "WARN", "ERROR"], // Add "DEBUG" for even more logging
	timeFormat: 24,
	units: "metric",

	modules: [

		{
			module: 'MMM-page-indicator',
			pages: {"pageNameOne": "bottom_bar", "pageNameTwo": "bottom_bar", "pageNameThree": "bottom_bar", "blank": "bottom_bar"},
			config: {
				pages: 2,
				activeBright: true,
			}
		},
		{
			module: "MMM-Page-Selector",
			position: "top_bar",
			config: {
				defaultPage: "pageNameOne",
				displayTitle: true,
			}
		},
		{
			module: "MMM-APOD",
			pages: {pageNameThree: "fullscreen_below"},
			config: {
				appid: "GfBH6tJ9nGeSzbWJ8pLCPwRg6gjahbMNiH9cSqxQ" // NASA API key (api.nasa.gov)
				
			}
		},
		{
			module: "alert",
		},
		{
			module: "updatenotification",
			pages: {"pageNameOne": "top_bar"},
		},
		{
			module: "clock",
			pages: {"pageNameOne": "top_left", },
		},
		{
			module: "calendar",
			header: "Schedule",
			pages: {"pageNameOne": "top_left"},
			config: {
				calendars: [
					{
						fetchInterval: 7 * 24 * 60 * 60 * 1000,
						symbol: "calendar-check",
						url: "webcal://p178-caldav.icloud.com/published/2/MjA2MDYyNTUxODQyMDYwNqZxAIF2XPkHkBjqdGpnjiqecnM7YtvzPdi30cmiesumT1f7vhNpT9QzPhpGKaYKmhHKFewdvhGFWx4zGexP1gw"
					}
				]
			}
		},
		{
			module: "compliments",
			pages: {"pageNameOne": "lower_third"},

		},
		{
			module: "weather",
			pages: {"pageNameOne": "top_right"},
			config: {
				weatherProvider: "openmeteo",
				type: "current",
				lat: 47.6061,
				lon: -122.3328,
			}
		},
		{
			module: "weather",
			pages: {"pageNameOne": "top_right"},
			header: "Weather Forecast",
			config: {
				weatherProvider: "openmeteo",
				type: "forecast",
				lat: 47.6061,
				lon: -122.3328,
			}
		},
		{
			module: "newsfeed",
			pages: {"pageNameOne": "top_center"},
			config: {
				feeds: [
					{
						title: "New York Times",
						url: "https://rss.nytimes.com/services/xml/rss/nyt/HomePage.xml"
					}
				],
				showSourceTitle: true,
				showPublishDate: true,
				broadcastNewsFeeds: true,
				broadcastNewsUpdates: true
			}
		},
	
		{
			/* Don't share your credentials! */
			module: "MMM-OnSpotify",
			pages: {"pageNameOne": "bottom_left" },
				config: {
				clientID: "16f92ba520be4e25b435507499a65ab8",
				clientSecret: "80acf8a97c21434aab4760788ce8fbee",
				accessToken: "BQARipBmW1pPlcTSEQaXfOURMugvCkDGrERmVSmsSXV9yWsnp2GBZJSwAYUPAKBLb4itI_qvv90XUO7S_9rToP0o_99Qd0P4WFanw6VUoX4-mCPenWtB9kWXd5f5bV-4X0Cg2KVoPb7-cM7PWwmoOmR_T0P7Qo2V2mcnzC-nZsiGIYz0US9V6H_WU9DJ0W38D6YkdrGHn0u1d-K7cFf3H2gEvkvyCOcHAvM",
				refreshToken: "AQDtmP28TaeahHee8i1OH1hPrPHgUUGxTfR1nWoyL4-NkK8KHb0HULhBuP7NJ3AjjJQCcUww2k51KVyegDvWMYETqh3a5FHNv1xbB0VpXe7hoxU8f0XB2DXqjIuf4VZGEzg",
				blurCorrectionInFrameSide: true,
				/* Add here your theming and behaviour configurations */

			}
		},
		{
			module: 'MMM-BackgroundSlideshow',
			pages: {PageNameOne: "fullscreen_below"},
			config: {
			  imagePaths: ['modules/MMM-BackgroundSlideshow/exampleImages/'],
			  transitionImages: true,
			  randomizeImageOrder: true
			}
		  },

		  
		  {
            module: 'MMM-Motion-Camera',
            config: {
                // See below for configurable options
            }
        },

	/*
			{
					module: 'voicecontrol',
					position: 'bottom_left',
					config: {
						models: [
							{
								keyword: "playMusic",   // keyword 
								description: "Say 'Play Music' to start playing",
								file: "playMusic.pmdl", // trained model file name
								message: "PLAY_MUSIC"   // notification message that's broadcast in the MagicMirror app
							},
							{
								keyword: "stopMusic",
								description: "Say 'Stop Music' to stop playing",
								file: "stopMusic.pmdl",
								message: "STOP_MUSIC"
							},
						]
					}
				},
		*/  
		/*{
			module: "MMM-Voice-Commands",
			config: {
				debug: false, //Displays end results and errors from annyang in the Log
				autoStart: true, //Adds annyang commands when it first starts
				activateCommand: "hello mirror", //Command to active all other commands
				deactivateCommand: "goodbye mirror", //Command to deactivate all other commands
				alertHeard: false, //Whether an alert should be shown when annyang hears a phrase (mostly for debug)
				commands: {
					"command statement :variable (optional statement)": "SOCKET_NOTIFICATION_NAME",
					//The payload of the socket notification will be whatever is said in the :variable
					"command statement *variable": function(param){
						alert("Whatever is said in the *variable space is given as the "+param);
						//These function's 'this' are bound to the module's 'this' so you can do stuff like:
						this.sendNotification("PAGE_SELECT", "2");
					}
				}
			}
		},*/
				{
					module: 'MMM-MovieInfo',
					pages: {"pageNameOne": "bottom_right"},
					config: {

						api_key: "7db38df1efe573c0fd5e9a5cfe1605e5",
        				
						
					}
				},

				{
					module: 'MMM-Globe',
					pages: {"pageNameTwo": "middle_center"},	// This can be any of the regions. Best results in lower_third
					config: {
							size:"medium", // Globe size. See configuration options below for more options
							dayLength: 50, // (Optional) Rotation speed. See configuration options below
							viewAngle: 15, // (Optional) Globe tilt. See configuration options below.
							locations: [ 
								// Fill with location Objects if desired
								// e.g.
								 {lat:37.77493,lng:-122.41942, label: "San Francisco"},
								 {lat:-23.5475,lng:-46.63611, label: "Sao Paulo"}
								
								// Individual values must be seperated by a comma. 
								// You can look up the latitude and longitude for a specific location on Google Maps.
							]
					}
				},
				
				
			  
				//Example of the config for a module to be shown on pages: "pageNameOne" and "pageNameTwo"
				
				
				/*{
					module: 'MMM-ProfileControl',
					position: 'bottom_bar',
					config: {
					  profiles: [
						['pageOneEveryone', 'pageOneBirthdays'],
						['pageTwoEveryone', 'pageTwoFamily', 'pageTwoLadies']
					  ],
				  
					  horizontalActiveIcon: 'fa-eye',
				  
					  notifications: {
						'pageOneEveryone' : [
						  {
							notification: 'HEY_THERE',
							payload: {
							  nobody: 'will react'
							}
						  },
						  {
							notification: 'HEY_THERE2',
						  }
						]
					  }
					}
				  },
				  */
				  {
					module: 'MMM-Hello-Mirror',
					position: 'lower_third',
					config: {
						// See 'Configuration options' for more information.
						voice: 'UK English Male',
						language: 'en'
					}
				},
				
				{
					module: "MMM-stoic-quotes",
					pages: {pageNameThree: "bottom_right"},
					config: {
						size: "medium",
						time: 60 * 60
					}
				},

				{
					disabled: false,
					module: 'MMM-lichess-daily',
					pages: {pageNameThree: "top_left"},
					config: {
					  // themes:
					  //   * blue
					  //   * blue2
					  //   * blue3
					  //   * canvas
					  //   * wood
					  //   * wood2
					  //   * wood3
					  //   * maple
					  //   * green
					  //   * marble
					  //   * brown
					  //   * leather
					  //   * grey
					  //   * metal
					  //   * olive
					  //   * purple
					  theme: "grey",
					  
					  backgrounds: "dark",
					  //   * light
					  //   * dark
					  bg: "auto",
					  width: "224px",
					  height: "264px",
					  updateInterval: 60 * 60 * 1000,
					}
				  },
				 
				  {
					module: "MMM-text-clock",
					pages: {pageNameThree: "upper_third"},
					config: {
					  // Options
						compact: true,
						size: "large",
					}
				  },
				  {
					module: 'planetrise',
					pages: {pageNameThree: "bottom_left"},	// This can be any of the regions.
					header: 'PLanet Rise',
					config: {  // Place the latitude and longitude of your mirror
						latitude: 47.6061,
						longitude: -122.3328,
						// A dictiory of the bodies and unicode character for the symbol
						// This is the default and does not need to be listed.
						// A full list of bodies can be seen on line 1359 in astronomy.js
						// Note: Trying to find the rise time of Earth will crash the Module
						bodies: {'Sun': '☉',
								'Moon': '☽',
								'Mercury': '☿',
								'Venus': '♀',
								'Mars': '♂',
								'Jupiter': '♃',
								'Saturn': '♄',
						}
					}
				},
				 
	]


	

	
};


/*************** DO NOT EDIT THE LINE BELOW ***************/
if (typeof module !== "undefined") { module.exports = config; }




```

# Bill of Materials


| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Raspberry Pi Kit | Powers the smart mirror | $97.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/RasTech-Raspberry-Starter-Heatsink-Screwdriver/dp/B0C8LV6VNZ/ref=sr_1_4?crid=3506HY00MCGVM&dib=eyJ2IjoiMSJ9._zkM62vSQ8p7tNr88715LdMv_qHh72Je-tkF9PXEa3chDE53QT4aZu4AGAb4ihE61QY4ZD55nKF6Fp2Kfs8t7AbafM_JrlJFfHo9OB4eAVGqa0EB-7aoBQHPmhKHZ2MW8ny-Kd44bMVlVxPlTWVk5YHIN5P3uKVqrE5Dcal0rKkHny-O6Xyb5ux2AOU6OwVbkag_bqBX66RQNRrgBuz-0pS43mcx93IZTQA9R8NaJJypYU2HAycp-XicTFmyU60a01Nfm9iuyo6B9yA8ppN3OQQyJ-NQ9xyNPxfTLwkqtng.yAYpU6outhQcZmOZhN9Wb6yTw7A85CNUbXZguGInZNg&dib_tag=se&keywords=raspberry%2Bpi%2Bkit&qid=1718848547&s=electronics&sprefix=rasbperry%2Bpi%2Bkit%2Celectronics%2C83&sr=1-4&th=1)"> Link </a> |
| Monitor | Displays the smart mirror | $45.99 | <a href="https://www.amazon.com/Hosyond-Display-1024%C3%97600-Capacitive-Raspberry/dp/B09XKC53NH/ref=sr_1_3?crid=1KKB9WC62OIAD&keywords=raspberry%2Bpi%2Bips&qid=1685911698&s=electronics&sprefix=raspberry%2Bpi%2Bips%2B%2Celectronics%2C87&sr=1-3&th=1"> Link </a> |
| Mouse and Keyboard | Navigating throughout the mirror | $19.99 | <a href="https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1"> Link </a> |
| Reflective film | What the item is used for | $5.88 | <a href="[https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1](https://www.amazon.com/dp/B0998PYXSH?ref=ppx_yo2ov_dt_b_product_details&th=1)"> Link </a> |
| Raspberry Pi Camera | Tracking | $13.50 | <a href="[https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1](https://www.amazon.com/Raspberry-Pi-Camera-Module-Megapixel/dp/B01ER2SKFS/ref=sr_1_3?crid=NIZ0NY56VFGO&dib=eyJ2IjoiMSJ9.SdZxeeuAaWgC9GeoeEJUFP62foW2SztM96rrEg7VSsaq9bv8a_rjpUd_qPS7VdG0zhD-QO70AYkKt6meJD3UZpHOMAv1p-hyGfKDdytwKB3S8EBCJj31NoxLKKkE22XbtM1Da8N_To08JJhv-UI8vUGxI0GboqyjFR6_bCzKtRckjlw3dB-lvp0T3B0l0a5SyTEZ-mOGz71HWITIIF4iUO6iCH7lPLvpdbPp9V-TxoU.e6NWpyU0y8PUPIyb1JteUTRKDHH1NWSsN2dbvr1VzQc&dib_tag=se&keywords=raspberry+pi+camera&qid=1723235264&sprefix=raspberry+pi+camera%2Caps%2C68&sr=8-3)"> Link </a> |
| Mouse and Keyboard | What the item is used for | $19.99 | <a href="https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1"> Link </a> |
| Mouse and Keyboard | What the item is used for | $19.99 | <a href="https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1"> Link </a> |

# Other Resources/Examples

- [3d Party Modules]([https://trashytuber.github.io/YimingJiaBlueStamp/](https://github.com/MagicMirrorOrg/MagicMirror/wiki/3rd-party-modules))


