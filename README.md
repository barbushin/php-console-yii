## PHP Console extension for Yii Framework

This extension integrates YII with Google Chrome extension [PHP Console](https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef)

## Requirements

* PHP 5.3 (or later)
* Yii Framework v1.* project
* Google Chrome extension [PHP Console](https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef)


## Installation

1. Copy "/src/extension/phpconsole"  to your extensions directory (i.e. /protected/extensions).
2. Copy "/src/vendors/PhpConsole"  to your vendors directory (i.e. /protected/vendors).
3. Modify your config file (i.e. /protected/config/main.php)

## Initialization & configuration

	'preload' => array('log'),
	
	'components' => array(

		'log' => array(
			'class' => 'CLogRouter',
			'routes' => array(
				'class' => 'ext.phpconsole.PhpConsoleLogRoute',
				/* Default options:
				'isEnabled' => true,
				'handleErrors' => true,
				'handleExceptions' => true,
				'sourcesBasePath' => $_SERVER['DOCUMENT_ROOT'],
				'phpConsolePathAlias' => 'application.vendors.PhpConsole.src.PhpConsole',
				'registerHelper' => true,
				'serverEncoding' => null,
				'headersLimit' => null,
				'password' => null,
				'enableSslOnlyMode' => false,
				'ipMasks' => array(),
				'dumperLevelLimit' => 5,
				'dumperItemsCountLimit' => 100,
				'dumperItemSizeLimit' => 5000,
				'dumperDumpSizeLimit' => 500000,
				'dumperDetectCallbacks' => true,
				'detectDumpTraceAndSource' => true,
				'isEvalEnabled' => false,
				*/
			)
		)
	)

## Usage

Try this code in some controller:


	// log using Yii methods
	Yii::log('There is some debug message');

	// log using PHP Console debug method
	PC::debug('Short way to debug directly in PHP Console', 'some,debug,tags');
	echo $undefinedVar;

## Resources

* [PHP Console homepage](https://github.com/barbushin/php-console)
* Google Chrome extension [PHP Console](https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef)
