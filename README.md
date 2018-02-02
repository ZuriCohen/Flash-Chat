# Flash-Chat

Beginner: Download the starter project files as .zip and extract the files to your desktop.

Pro: Git clone to your Xcode projects folder.

## First Podfile Configuration
```
post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['CLANG_WARN_DOCUMENTATION_COMMENTS'] = 'NO'
        end
    end
end
```


## Second Podfile Configuration
```
    pod 'SVProgressHUD', :inhibit_warnings => true

```


## Finished Podfile Configuration
```
    platform :ios, '9.0'

target 'Flash Chat' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

    pod 'Firebase'
    pod 'Firebase/Auth'
    pod 'Firebase/Database'
    pod 'SVProgressHUD', :inhibit_warnings => true
    pod 'ChameleonFramework'

end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['CLANG_WARN_DOCUMENTATION_COMMENTS'] = 'NO'
        end
    end
end


```


## Finished App
![Finished App](https://github.com/blakazulu/Images/blob/master/Flash%20Chat.gif)



Copyright © The App Brewery
