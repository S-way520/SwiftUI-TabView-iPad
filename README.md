# SwiftUI-TabView-iPad
SwiftUI TabView bottom button only iPad swift playground
# The first part
![IMG_1229](https://github.com/S-way520/SwiftUI-TabView-iPad/assets/95877651/7652db7d-5c0c-4a62-9712-458660a01e0b)

# The second part
Code file 1
```swift
import SwiftUI
@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            Bar()
        }
    }
}
```
Code file 2
```swift
import SwiftUI
struct Bar: View {
    var body: some View {
        TabView {
            OneView().tabItem {
                Image(systemName: "house")
                Text("主页")
            }
            TwoView().tabItem{
                Image(systemName: "mappin.and.ellipse")
                Text("周边")
            }
            ThreeView().tabItem{
                Image(systemName: "person.fill")
                Text("我的")
            }
        }
        .edgesIgnoringSafeArea(.all)
        .accentColor(Color.red)//Button Color
        .onAppear(perform: {
            UITabBar.appearance().backgroundImage = UIImage()
            UITabBar.appearance().shadowImage = UIImage()
            //UITabBar.appearance().unselectedItemTintColor = UIColor.gray
        })
    }
}
```
Code file 3
```swift
import SwiftUI
struct OneView:View {
    var body: some View {
        Text("One")
    }
}
```
Code file 4
```swift
import SwiftUI
struct TwoView:View {
    var body: some View {
        Text("Two")
    }
}
```
Code file 5
```swift
import SwiftUI
struct ThreeView:View {
    var body: some View {
        Text("Three")
    }
}
```
