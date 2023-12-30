Hayek browser is forked from brave browser
# Download and compile Hayek Browser

Hayek browser is forked from brave browser.
system requier:Ubuntu 22.4 or above
node version: 16.17.1
```bash
git config --global --unset http.proxy
git config --global --unset https.proxy
export http_proxy=
export https_proxy=
git config --global core.compression 0 
#set git no  compression,remove all proxy setting.

mkdir hayekbrowser/src/brave
cd  hayekbrowser/src
git clone https://github.com/yianding/brave-core.git ./brave
cd brave 
npm install
npm run init -- --target_os=android --target_arch=arm
#waiting for sync chromium project.very long time depends on your internet speed.

npm run build gen_gradle

# after buid, 
cd  cd ../out/android_gen_gradle_arm/apks/
# install apk to your android device
adb install ChromePublic.apk
#very long time depends on your CPU and memory.

```




# Brave Core

Brave Core is a set of changes, APIs, and scripts used for customizing Chromium to make the Brave browser. Please also check https://github.com/brave/brave-browser

Follow [@brave](https://twitter.com/brave) on Twitter for important announcements.

## Resources

- [Issues](https://github.com/brave/brave-browser/issues)
- [Releases](https://github.com/brave/brave-browser/releases)
- [Documentation wiki](https://github.com/brave/brave-browser/wiki)

## Community

You can ask questions and interact with the community in the following
locations:
- [Brave Community](https://community.brave.com/)
- [`community`](https://bravesoftware.slack.com) channel on Brave Software's Slack
