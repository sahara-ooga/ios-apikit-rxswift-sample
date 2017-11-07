# ios-apikit-rxswift-sample
sample app using APIKit, RxSwift

## Library instration via Carthage
### Cartfile
In the project folder, make `Cartfile` like:

```
github "ishkawa/APIKit" ~> 3.1
github "ReactiveX/RxSwift" ~> 4.0
```

Then, `$ carthage update`

### Xcode settings
First, move to project, [General] tab.

In [Link Binary With Libraries], add needed frameworks.

Move to [Build Phases] tab.

In [Run Script], add `/usr/local/bin/carthage copy-frameworks`

In [Input Files], add

```
$(SRCROOT)/Carthage/Build/iOS/Result.framework
$(SRCROOT)/Carthage/Build/iOS/APIKit.framework
$(SRCROOT)/Carthage/Build/iOS/RxCocoa.framework
$(SRCROOT)/Carthage/Build/iOS/RxSwift.framework
$(SRCROOT)/Carthage/Build/iOS/RxTest.framework
$(SRCROOT)/Carthage/Build/iOS/RxBlocking.framework
```

In [Output Files], add

```
$(DERIVED_FILE_DIR)/$(FRAMEWORKS_FOLDER_PATH)/Result.framework
$(DERIVED_FILE_DIR)/$(FRAMEWORKS_FOLDER_PATH)/APIKit.framework
$(DERIVED_FILE_DIR)/$(FRAMEWORKS_FOLDER_PATH)/RxCocoa.framework
$(DERIVED_FILE_DIR)/$(FRAMEWORKS_FOLDER_PATH)/RxSwift.framework
$(DERIVED_FILE_DIR)/$(FRAMEWORKS_FOLDER_PATH)/RxTest.framework
$(DERIVED_FILE_DIR)/$(FRAMEWORKS_FOLDER_PATH)/RxBlocking.framework
```

If you need them in unit tests, Unit test target require same settings.

## Reference
- [APIKit (Github)](https://github.com/ishkawa/APIKit)
- [RxSwift (Github)](https://github.com/ReactiveX/RxSwift/)
- [Carthage (Github)](https://github.com/Carthage/Carthage/)

## Environment
- Xcode 9
- Swift 4
- iOS 11