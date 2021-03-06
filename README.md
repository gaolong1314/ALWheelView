# ALWheelView
[![CocoaPods](https://img.shields.io/cocoapods/l/ALWheelView.svg)](https://raw.githubusercontent.com/AshStill/ALWheelView/master/README.md)&nbsp;
[![CocoaPods](https://img.shields.io/cocoapods/v/ALWheelView.svg)](http://cocoapods.org/?q=ALWheelView)&nbsp;
[![CocoaPods](https://img.shields.io/cocoapods/p/ALWheelView.svg)](http://cocoapods.org/?q=ALWheelView)&nbsp;
[![Support](https://img.shields.io/badge/support-iOS%207%2B-blue.svg)]()&nbsp;

A WheelView based on UICollectionView.
* Customize View as using collectionView
* UICollectionView-like delegates
* Customize radius/size/scale
* Infinite loop

![image](https://github.com/AshStill/ALWheelView/blob/master/screenshot.gif)

## Pod
    pod 'ALWheelView'

## Usage
#### init view and assign the delegate
     - (ALWheelView *)wheelView
    {
        if (!_wheelView) {
            _wheelView = [[ALWheelView alloc] initWithFrame:CGRectMake(0, 0, CGRectGetWidth(self.view.bounds), CGRectGetHeight(self.view.bounds))];
            _wheelView.delegate = self;
        }
        return _wheelView;
    }
    
#### implement the delegates below
    - (NSInteger)numberOfItemsInWheel:(ALWheelView*)wheelView;
    - (CGFloat)radiusOfWheel:(ALWheelView*)wheelView;
    - (CGFloat)minScaleOfItemInWheel:(ALWheelView*)wheelView;
    - (CGSize)sizeOfItemInWheel:(ALWheelView*)wheelView atIndex:(NSInteger)index;
    - (void)wheelView:(ALWheelView*)wheelView didClickItemAtIndex:(NSInteger)index;
    - (UIView*)wheelView:(ALWheelView*)wheelView itemViewAtIndex:(NSInteger)index;
    - (void)wheelViewWillBeginDragging:(ALWheelView*)wheelView;
    - (void)wheelViewDidEndScrollAnimation:(ALWheelView*)wheelView;


## Release Note

**0.1.0**
* Basic delegates
* Infinite loop
