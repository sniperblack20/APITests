# APITests
APITests is a simple automation framework demonstrating the use of newman to run a collection of postman tests.

## Newman
Newman is a command-line collection runner for Postman. It allows you to effortlessly run and test a Postman collection directly from the command-line.

## Installing Newman
To run Newman, ensure that you have [Node.js >= v10](https://nodejs.org/en/download/)

The easiest way to install [Newman](https://github.com/postmanlabs/newman) is using NPM. If you have Node.js installed, it is most likely that you have NPM installed as well.

```console
$ npm install -g newman
```

This installs Newman globally on your system allowing you to run it from anywhere. If you want to install it locally, Just remove the -g flag.

## Newman reporter
An optional reporter can be added to newman to generate some Test artifacts (test results).

To install:

```console
$ npm install -g newman-reporter-html
```

## Prerequisites in running the test
1. Trademe Sandbox account
2. Trademe sandbox Oauth tokens (for the sake of executing these tests, I included my tokens in a environment.json file)

## To run these tests

1. Clone this repo

```console
$ git clone https://github.com/sniperblack20/APITests.git
```

2. Navigate to where the project was downloaded.

3. Run in the command line using:

Syntax:
```console
$ newman run <tests> -e <environment files> -k -r html
```

where
| Parameter | Description |
|-----------|-------------|
| tests 	| path to collection of json files containing the tests |
| environment files | path to collection of environment related files |
| -e 		| environment parameter |
| -r 		| invoke the reporter |
| html		| reporter type	|

like this:
```console
$ newman run Collections/Trademe\ -\ Used\ Motors\ Tests.json -e Environment/environment.json -k -r html
```

Notes:
1. The collection name is "Trademe - Used Motors Tests.json"
2. The tokens needed for this test are included in the environment.json file.
3. HTML reports will be generated in newman/ folder.

## Contributing
Pull requests are not welcome. This repo is for my personal consumption only. It may be removed without prior notice.
