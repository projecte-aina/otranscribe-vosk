## oTranscribe+

Despite the advances in machine learning applications, specifically Automatic Speech Recognition (ASR), the language work based within the audiovisual sector such as transcription, translation and subtitling still relies on manual labor done by experts. During the last decade, the inclusion of the new technologies only contributed to the Computer Assisted Transcription technologies, through the appearance of new startups which combine ASR and related technologies (speaker diarization, punctuation and capitalization recovery etc.) with an online editor. 

However, there is a barrier of entry to the adoption of these tools, mostly due to their cost reflected on the client, which are priced based on the length of audio to be processed/transcribed. We aim to present a low-cost alternative to these platforms, both for the final user and the provider; taking advantage of the latest developments in the speech technologies, namely the use of edge (client-side) computing and open ASR models which are small and precise.

With this platform/tool, language workers can upload a file to the web application and receive a basic transcription. Since ASR decoding is done on client-side, the provider can serve multiple users without the concern on costs per user computationally; since the server side processes will be limited.

oTranscribe+ is an **[oTranscribe](http://oTranscribe.com/)** fork that adds [Vosk-Browser](https://github.com/ccoreilly/vosk-browser) functionality.

## Extended version

### Requirements

This project requires Node version 12. We recommend to use the [Node Version Manager](https://github.com/nvm-sh/nvm) tool, as well as the [Yarn](https://yarnpkg.com/) package manager. With them you can locally use that Node version 12 and install requirements:

```
nvm use 12
yarn install
```

### Usage and compilation

Code lives in `src` folder. There you will find the raw JavaScript and CSS files. Before you start expanding them you need to be using Node version 12 and have requirements already installed. Then, for compiling the code, obtaining a sourcemap, and 'watch-for-changes', run `make build_dev`.

`dist` folder will be filled with the end result of oTranscribe+ files and folders. You can emulate the access by a remote browser launching on that location the next Python command: `python3 -m http.server`. Having run this, you will be able to access with your browser to your local port 8000, where oTranscribe+ should be served.

### Compile the production-ready files

- Install [Node.js and NPM](https://nodejs.org).
- Run `npm install` to install dependencies
- Run `make build_prod` to compile the `dist` folder

### OTR file format

oTranscribe has its own file format (.otr), which is just a JSON file with the following parameters:

* **text**: The raw HTML of the transcript
* **media**: If available, the name of the last media used
* **media-source**: If available, a link to the last media used
* **media-time**: If available, the playtime of the last media used

### Running tests

oTranscribe is not fully tested. There are only a small number of tests, for data migration.

To setup, [install CasperJS](http://docs.casperjs.org/en/latest/installation.html).

Then run a server at the root directory of this repository at `http://localhost:8000`, and on the command line run:

    casperjs test tests/

## oTranscribe translations

Translations have been provided by the following talented and generous volunteers:

*   Catalan: [Joan Montané](http://www.softcatala.org/wiki/Usuari:Jmontane) and [Jon Sindreu](https://twitter.com/jonsindreu).
*   Chinese: baiqj, Cindy Ng, [Andy Pan](https://github.com/andy0130tw), [Cp0204](https://github.com/Cp0204) and [Robin Kwong](https://github.com/RobinKwong)
*   Danish: [Christian Bruun](http://christianb.dk).
*   Dutch: [Patrick Mackaaij](http://www.eenmanierom.nl) and Marjolein Quist.
*   Filipino: [Patricia Albano](https://www.linkedin.com/in/patriciaclaudiaalbano).
*   French: [Olivier Aubert](http://www.olivieraubert.net), [@goofy-bz](https://github.com/goofy-bz) and [Dr J Rogel-Salazar](http://quantumtunnel.wordpress.com).
*   German: [Dr J Rogel-Salazar](http://quantumtunnel.wordpress.com) and Lisa Bernhardt.
*   Indonesian: [Joy Tikoalu](mailto:joy.tikoalu@gmail.com).
*   Italian: [Dr J Rogel-Salazar](http://quantumtunnel.wordpress.com), [Edoardo Putti](http://edoput.it) and Federico Lasta.
*   Japanese: [harupong](http://blog.harupong.com).
*   Norwegian: [Hallvar Hauge Johnsen](http://www.hyggelaget.no/)
*   Polish: Emil Maruszczak and Piotr Tarasewicz.
*   Portuguese: [enVide neFelibata](http://www.envidenefelibata.com).
*   Brazilian Portuguese: Leonardo Barichello and [Carlos Eduardo Pinheiro Rocha](https://www.linkedin.com/in/carlos-eduardo-pinheiro-rocha-1756395b/).
*   Romanian: [Iain Apreotesei](https://github.com/ibriq) and [Catalina Albeanu](https://twitter.com/catalinacma)
*   Russian: [Pavel Osminin](http://www.proz.com/profile/1783004)
*   Spanish: [Cristian Duque](https://github.com/crskkk), [Dr J Rogel-Salazar](http://quantumtunnel.wordpress.com) and [Adrián Blanco](https://twitter.com/AdrianBlancoR).
*   Swedish: c3ons.
*   Turkish: Mehmet S. DERİNDERE. 
*   Ukrainian: [Myroslav Opyr](https://github.com/myroslav)
*   Vietnamese: [Trần Ngọc Quân](https://github.com/vnwildman)
*   Greek: [Konstantinos Alexiou](http://konalexiou.net)

More about translating oTranscribe [here](https://github.com/oTranscribe/oTranscribe/wiki/Help-translate-oTranscribe).
