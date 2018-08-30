# Marion's updated Stack Overflow theme for JSONresume

## Getting started

### Install the command line

Create your resume in json on [jsonresume](https://jsonresume.org)

The official [resume-cli](https://github.com/jsonresume/resume-cli) to run the development server.

Go ahead and install it:

```
sudo npm install -g resume-cli
```

### Build / export your resume

Install the theme:
```
npm install -g jsonresume-theme-stackoverflow-marion
```

Export resume with this theme:
```
resume export resume.html --them stackoverflow-marion
```

You should have a `resume.html` file with the correct theme.

### Developement (Install and serve theme with hot reloading)

Clone the repository and install deps:

```
npm install
```

Serve:

```
resume serve
```

You should now see this message:

```
Preview: http://localhost:4000
Press ctrl-c to stop
```

To build your own resume, create a 'resume.json' file in the current folder and follow the [json resume schema](https://jsonresume.org/schema/)

### Social Profiles Icons

**Profiles supported with brand colors:**

github, stack overflow, linkedin, dribbble, twitter, facebook, pinterest, instagram, soundcloud, wordpress, youtube, flickr, google plus, tumblr, foursquare.

To have a social icon close the social link profile (or username) it is enough to set a `network` the name of the Social Network (es: 'Stack Overflow').

> Note: you can use the *custom field* `icon` to set a custom Font Awesome icon. For example, devpost doesn't have a social icon yet, so you can give it a custom icon like this:
```
profiles: [
  {
    "network": "Devpost",
    "icon": "fas fa-code",
    "username": "marionleborgne",
    "url": "https://devpost.com/marionleborgne"
  }
]
```

#### Support to extra fields

With stackoverflow theme it is possible to add:

- `keywords` to each 'work', 'publication' and 'volunteer' item
- `summary` to each 'interests' and 'education' item
- `location` to each 'work', 'education' and 'volunteer' item
- `birth` to 'basics'

example of the extra `location` object: 

```
"location": {
  "city": "Zürich",
  "countryCode": "CH",
  "region": "Switzerland"
} 
```
example of the extra `birth` object:

```
"birth": {
  "place": "New York",
  "state": "USA",
  "date": "1988"
}
```

## Contribution

Fork the project, add your feature (or fix your bug) and open a pull request OR

[Open an issue](https://github.com/francescoes/jsonresume-theme-stackoverflow/issues/new) if you find find or if you would like to have extra fields or changes 

## License

Available under the [MIT license](http://opensource.org/licenses/mit-license.php).
