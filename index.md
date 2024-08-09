# Smart Mirror Project
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| FirstName LastInitialOnly | School Name | Electrical Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone



<iframe width="560" height="315" src="https://www.youtube.com/embed/pFjmpbU6Lu8?si=69HFv4WDD_iIQSxV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

# First Milestone



<iframe width="560" height="315" src="https://www.youtube.com/embed/vAhzwOk_3u8?si=VIA64c6HJX5M6EU7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


My project is the Smart Mirror, which uses an open source modular smart mirror platform called Magic Mirror. The Smart Mirror is powered by raspberry pi and is displayed on a HDMI monitor. So far I have finished the basis of the smart mirror and added and changed a few modules. I added a spotify module which is connected to my spotify account as well as a background module that allows me to put different background images on my Smart Mirror. I also modified the size and the place of certain modules on the mirror so that all the modules are displayed normally. 

A few challenges I have been finding are learning different commands to add modules and changing the placement of certain modules. Adding modules requires me to put certain commands into the raspberry pi terminal which I have never done before, and modifying modules was difficult as each module has many files in different coding languages such as CSS and Javascript that affect module placement and function.

I hope to implement a few more modules onto my smart mirror to improve the variety of functions my smart mirror can display. I'm also interested in adding a camera to the mirror or speakers and microphone so that I can code the Smart Mirror to react to certain sounds or movements.


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

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
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Raspberry Pi Kit | Powers the smart mirror | $97.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/RasTech-Raspberry-Starter-Heatsink-Screwdriver/dp/B0C8LV6VNZ/ref=sr_1_4?crid=3506HY00MCGVM&dib=eyJ2IjoiMSJ9._zkM62vSQ8p7tNr88715LdMv_qHh72Je-tkF9PXEa3chDE53QT4aZu4AGAb4ihE61QY4ZD55nKF6Fp2Kfs8t7AbafM_JrlJFfHo9OB4eAVGqa0EB-7aoBQHPmhKHZ2MW8ny-Kd44bMVlVxPlTWVk5YHIN5P3uKVqrE5Dcal0rKkHny-O6Xyb5ux2AOU6OwVbkag_bqBX66RQNRrgBuz-0pS43mcx93IZTQA9R8NaJJypYU2HAycp-XicTFmyU60a01Nfm9iuyo6B9yA8ppN3OQQyJ-NQ9xyNPxfTLwkqtng.yAYpU6outhQcZmOZhN9Wb6yTw7A85CNUbXZguGInZNg&dib_tag=se&keywords=raspberry%2Bpi%2Bkit&qid=1718848547&s=electronics&sprefix=rasbperry%2Bpi%2Bkit%2Celectronics%2C83&sr=1-4&th=1)"> Link </a> |
| Monitor | Displays the smart mirror | $45.99 | <a href="https://www.amazon.com/Hosyond-Display-1024%C3%97600-Capacitive-Raspberry/dp/B09XKC53NH/ref=sr_1_3?crid=1KKB9WC62OIAD&keywords=raspberry%2Bpi%2Bips&qid=1685911698&s=electronics&sprefix=raspberry%2Bpi%2Bips%2B%2Celectronics%2C87&sr=1-3&th=1"> Link </a> |
| Mouse and Keyboard | What the item is used for | $19.99 | <a href="https://www.amazon.com/gp/product/B07XDWCLYF/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
