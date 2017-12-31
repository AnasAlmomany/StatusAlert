![Author StatusAlert](https://assets.gitlab-static.net/ZEBSTER/FrameworksAssets/raw/master/StatusAlert/StatusAlertHeader.png)

[![Swift](https://img.shields.io/badge/Swift-4.0-orange.svg?style=flat)]()
[![Version](https://img.shields.io/cocoapods/v/StatusAlert.svg?style=flat)](http://cocoapods.org/pods/StatusAlert)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![License](https://img.shields.io/cocoapods/l/StatusAlert.svg?style=flat)](http://cocoapods.org/pods/StatusAlert)
[![Platform](https://img.shields.io/cocoapods/p/StatusAlert.svg?style=flat)](http://cocoapods.org/pods/StatusAlert)

StatusAlert is an iOS framework that displays status alerts similar to Apple's system self-hiding alerts. It is well suited for notifying user without interrupting user flow in iOS-like way.

It looks very similar to the alerts displayed in Podcasts, Apple Music and News apps.
![System StatusAlert](Assets/iPhonesWithSystemAlerts.png)

 - [Features](#features)
 - [Requirements](#requirements)
 - [Installation](#installation)
	- [CocoaPods](#cocoapods)
	- [Carthage](#carthage)
 - [Demo](#demo)
 - [Usage](#usage)
 - [Customization](#customization)
 	- [Different configurations](#different-configurations)
 	- [Vertical position](#vertical-position)
 	- [Appearance](#appearance)
 	- [Dismissal](#dismissal)
 - [Apps Using _StatusAlert_](#apps-using-statusalert)
 - [Author](#author)
 - [License](#license)

## Features

* System-like look and feel
* "Reduce transparency" mode support
* Safe Areas support
* Universal (iPhone & iPad)

## Requirements

* Xcode 9.0 or later
* iOS 9.0 or later
* Swift 4.0

## Installation

StatusAlert is available via CocoaPods and Carthage.

### CocoaPods

To install StatusAlert using [CocoaPods](http://cocoapods.org), add the following line to your `Podfile`:

```ruby
pod 'StatusAlert', '~> 0.9.3'
```

### Carthage

To install StatusAlert using [Carthage](https://github.com/Carthage/Carthage), add the following line to your `Cartfile`:

```ruby
github "LowKostKustomz/StatusAlert" ~> 0.9.3
```

## Demo

Demo application is included in the `StatusAlert` workspace. To run it clone the repo.

![Demo StatusAlert](Assets/iPhonesWithStatusAlert.png)

## Usage

```swift
// Importing framework
import StatusAlert

// Creating StatusAlert instance
let statusAlert = StatusAlert.instantiate(withImage: UIImage(named: "Some image name"),
					  title: "StatusAlert title",
					  message: "Message to show beyond title",
					  canBePickedOrDismissed: isUserInteractionAllowed)

// Presenting created instance
statusAlert.show(in: viewShowAlertIn,
		 withVerticalPosition: .center(offset: 0))
```
> All the alert components (`image`, `title`, `message`) are optional, but at least one should be present. Otherwise `show()` method will be ignored.
>
> **IMPORTANT**
>  > The alert must be presented only from the main thread, otherwise application will crash with an appropriate error.

## Customization

### Different configurations

Present alert with any set of image, title and message

### Vertical position

Display alert anywhere you want, either on the top, in the center or at the bottom of the view, and with any offset.

### Appearance

You can customize a single alert's appearance via the `StatusAlert`'s properties

```swift
public var titleFont: UIFont
public var messageFont: UIFont
public var contentColor: UIColor
```
or for all alerts at once with `StatusAlert.Appearance`'s properties

```swift
public static var titleFont: UIFont
public static var messageFont: UIFont
public static var contentColor: UIColor
```

### Dismissal

Alert will hide itself after 2 seconds timeout.

You can also pass `canBePickedOrDismissed: true` into `StatusAlert`'s `instantiate` method. After that you will also be able to dismiss the alert manually by tap it and long tap the alert to delay dismissal.

## Apps Using _StatusAlert_

[BitxfyAppStoreLink]: https://itunes.apple.com/us/app/bitxfy-bitcoin-wallet/id1326910438?ls=1&mt=8

### • <img src="Assets/BitxfyIcon.png" align="center" width="40"> [Bitxfy][BitxfyAppstoreLink]

[![BitxfyScreenShot](Assets/BitxfyStatusAlert.png)][BitxfyAppstoreLink]

> Feel free to submit pull request if you are using this framework in your apps.

## Author

[FrameworksRepo]: https://github.com/LowKostKustomz/Frameworks

![Author ActionsList](https://assets.gitlab-static.net/ZEBSTER/FrameworksAssets/raw/master/ActionsList/ActionsListAuthor.png)

[<img src="https://assets.gitlab-static.net/ZEBSTER/FrameworksAssets/raw/master/Socials/Twitter.png" width="80">](https://twitter.com/LowKostKustomz)
[<img src="https://assets.gitlab-static.net/ZEBSTER/FrameworksAssets/raw/master/Socials/Email.png" width="80">](mierosh@gmail.com)
[<img src="https://assets.gitlab-static.net/ZEBSTER/FrameworksAssets/raw/master/Socials/Portfolio.png" width="80">][FrameworksRepo]

## License

> The MIT License (MIT)
>
> Copyright (c) 2017 LowKostKustomz <mierosh@gmail.com>
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
> 
> The above copyright notice and this permission notice shall be included in
> all copies or substantial portions of the Software.
> 
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
> THE SOFTWARE.