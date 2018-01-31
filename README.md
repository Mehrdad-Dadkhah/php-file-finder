# php-file-finder

[![Software License](https://img.shields.io/badge/license-GPL-brightgreen.svg?style=flat-square)](LICENSE)
[![Packagist Version](https://img.shields.io/packagist/v/Mehrdad-Dadkhah/php-file-finder.svg?style=flat-square)](https://packagist.org/packages/mehrdad-dadkhah/php-file-finder)


simple package to find file or directory full path and related information in php 


## Installation

```
composer require mehrdad-dadkhah/php-file-finder
```

## Usage
```PHP
use MehrdadDadkhah\File\Finder;

$finder = new Finder();

```

can change finder, default is `find` and can change it to `locate`

```PHP
$finder->setFinder('locate');
```

find with filename and search all directories:

```PHP
$finder->findFile('myFile.mp4', '/');
```

find all video(mp4) files in /home dir:

```PHP
$finder->findFile('*.mp4', '/home');
```

find a file with it's related path:

```PHP
$finder->findFile('related/path/to/files/myFile.mp4');
```

find files and only return file path without extra information:

```PHP
$finder->findFile('myFile.mp4', '/', false);
```

find directory with name test:

```PHP
$finder->findDirectoryPath('test', '/');
```


## License

hls-video-generater is licensed under the [GPLv3 License](http://opensource.org/licenses/GPL).