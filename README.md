# LCNavigator

## 介绍

一个简单的方便页面控制器之间跳转的工具~✌️

## 通过CocoaPods安装

```ruby
pod 'LCNavigator'
```

## 主要方法

```
@interface LCNavigator : NSObject

#pragma mark - 传参说明（id可传类型：UIViewController对象/NSString/[UIViewController class]）

#pragma mark - Push/Present

+ (void)push:(id)viewController;
+ (void)push:(id)viewController animated:(BOOL)animated;
+ (void)push:(id)viewController extraParams:(NSDictionary *)extraParams;
+ (void)push:(id)viewController extraParams:(NSDictionary *)extraParams animated:(BOOL)animated;

+ (void)present:(id)viewController;
+ (void)present:(id)viewController animated:(BOOL)animated;
+ (void)present:(id)viewController extraParams:(NSDictionary *)extraParams;
+ (void)present:(id)viewController extraParams:(NSDictionary *)extraParams animated:(BOOL)animated;

#pragma mark - Pop

+ (void)pop;
+ (void)pop:(BOOL)animated;
+ (void)popToRoot;
+ (void)popToRootAnimated:(BOOL)animated;
+ (void)popTo:(id)viewController;
+ (void)popTo:(id)viewController animated:(BOOL)animated;

#pragma mark - 获取

/** 获取当前nav */
+ (UINavigationController *)currentNavigationController;
/** 获取当前vc */
+ (UIViewController *)currentViewController;


/** 获取某个vc */
+ (UIViewController *)controllerWith:(id)viewController;
+ (UIViewController *)controllerWith:(id)viewController extraParams:(NSDictionary *)extraParams;

#pragma mark - Method

/** 判断是否是当前vc(只判断是同一个类,不区分是否是同一个对象) */
+ (BOOL)isMemberOfCurrentVC:(id)viewController;

@end
```

## Author

LuckyCat, https://github.com/LuckyCat7848/Blogs

## License

LCNavigator is available under the MIT license. See the LICENSE file for more info.
