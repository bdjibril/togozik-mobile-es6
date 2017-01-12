Experiments with tabris.js ES6 + Declarative UI
===============================================

# ES6 + Declarative UI

```javascript
/*************************
 * Import Components
 *************************/
import { Text, Composite, Image} from './tabris/components';


function BookDetails(book) {
	return (
		Composite( bookDetailsStyle.container,[
			Image( book.image, bookDetailsStyle.image, fadeIn(800) ),
			Composite( bookDetailsStyle.textContainer , [
				Text( book.title , bookDetailsStyle.title  , fadeInRight(500, 100) ),
				Text( book.author, bookDetailsStyle.author , fadeInRight(500, 300) ),
				Text( book.price , bookDetailsStyle.price  , fadeInRight(500, 500) )
			])
		]).on("tap",  () => { openReadBookPage(book) })
	)
}
```

![Native UI demo](https://tabrisjs.com/assets/public-content/img/examples/bookstore.gif)


# Setup

Seting up is really easy (you just node node installed):

```shell
$ git clone https://github.com/eclipsesource/tabris-js-experiments.git
$ cd tabris-js-experiments
$ npm install
$ npm run build
$ npm run watch
```

And in a new shell inside the tabris-js-experiments directory:
```shell
$ npm install -g http-server
$ http-server
```
Connect to your code from the Tabris.js Developer App ([Play Store](https://play.google.com/store/apps/details?id=com.eclipsesource.tabris.js) / [App Store](https://itunes.apple.com/us/app/tabris.js/id939600018?ls=1&mt=8)).

# Contribute

Please read the related blog post on: [Eclipsesource Blog](http://eclipsesource.com/blogs/2016/02/29/tabris-js-declarative-ui-in-100-lines-of-functional-programming/)

For any questions ping me: shai@eclipsesource.com

# Thanks

- [Gianluca Guarini - ES6 Project Starter Kit](https://github.com/GianlucaGuarini/es6-project-starter-kit)
