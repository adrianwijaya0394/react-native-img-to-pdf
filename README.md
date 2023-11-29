
# react-native-img-to-pdf

Create a PDF by an Array of images in React-Native.

## Getting started

`$ npm install react-native-img-to-pdf --save`

or

`$ yarn add react-native-img-to-pdf`

## Usage
```javascript
import RNImageToPdf from 'react-native-img-to-pdf';

...
const myAsyncPDFFunction = async () => {
	try {
		const options = {
			imagePaths: imagePaths: ['/path/to/image1.png','/path/to/image2.png'],
			name: name: 'PDFName',
			maxSize: { // optional maximum image dimension - larger images will be resized
				width: 900,
				height: Math.round(deviceHeight() / deviceWidth() * 900),
			},
			quality: .7, // optional compression paramter
		};
		const pdf = await RNImageToPdf.createPDFbyImages(options);
		
		console.log(pdf.filePath);
	} catch(e) {
		console.log(e);
	}
}
```
  
