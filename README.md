# Japanese License Plate Generator for Model Cars
Script to generate a Japanese license plate for model car (duh)

## Table of Content
- [Description](#Description)
- [Example](#Example)
- [Tasklist](#Tasklist)
- [Possible improvements](#Possible-improvements)
- [References](#References)
- [Changelog](#Changelog)
## Description
The goal here is to make a script that allows me to quickly generate a license plate for me to print for my model cars as trying to do everything in Illustrator is much more harder to do for some other fellow modellers.

Prior to this we had always used [this used-to-be-free site](https://minicarmuseum.com/platecreate.php) to create plate as their tool is much more elaborate in terms of options. However, they had now implemented a paywall so I've decided to move my lazy ass to create a script to do the work

This project uses [Python PIL Library](https://github.com/python-pillow/Pillow) to generate the plate itself.

I only managed to find two font projects that aim to recreate Japanese License plate font, which is:
- [TRM Font guide by Mr. T](http://dc-crafts.main.jp/trm/f/trmfont-jb.html)
- [FZ Number Plate font by フォントプロジェクト](http://expwyandstamps.web.fc2.com/sozai/fontproject.htm)

If you have more, feel free to let me know.

P/S: This is my first time dipping my toe into Python. plsdontbeharshtometq

## Example

Generated with v0.01 script

<img src="/resource/example/example.png?raw=true" width="300"/>

Actual License plate

<img src="/resource/example/example2.jpg?raw=true" width="300"/>

## Tasklist
- [x] Let the script use both TRM & FZ font depending on Land Transport Office Abbreviation （陸運支局略称）
- [ ] Create a list of available abbreviations and allow user to choose class number （分類番号）
- [x] Make different background & font color for *kei* cars, commercial vehicles and *kei* commercial vehicles
- [ ] Create a list of available Hiragana/English letter (for Okinawa plates) to be used in plates
- [x] Make font size for the hiragana character in both font to be uniform
- [ ] Create a field to allow user to choose whatever number they want
- [ ] Create a user interface for this application/script

## Possible improvements

- Generate a printable PDF file that changes size dynamically to accomodate 1/18 scale all the way to 1/100 scale
- Make the script a discord bot that allows mobile user to use the script
- Make more abbreviations as the ones supplied by TRM and FZ is quite lacking (only 18 in both font combined compared to close to 100 that the official one has)
- Make more hiragana character as the one supplied by TRM and FZ is quite limited
- Make the script for other countries such as Thailand (because Thai plates more widely used by modellers)

## References
- [Japan Number Plate Abbreviation List](https://ja.wikipedia.org/wiki/%E6%97%A5%E6%9C%AC%E3%81%AE%E3%83%8A%E3%83%B3%E3%83%90%E3%83%BC%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E4%B8%80%E8%A6%A7)
- [TRM Font guide by Mr. T](http://dc-crafts.main.jp/trm/f/trmfont-jb.html)
- [FZ Number Plate font by フォントプロジェクト](http://expwyandstamps.web.fc2.com/sozai/fontproject.htm)
- [Python PIL Library](https://github.com/python-pillow/Pillow)

## Changelog

### v0.02
- Made various element of a plate into components
- Created "Plate" class to better manage everything
- Created different background for different classes
- Font changes by supported LTO Abbreviation of each font
- Both TRM FZ font should now change dynamically based on supported element

### v0.01
- Created the basic mechanism of the script
