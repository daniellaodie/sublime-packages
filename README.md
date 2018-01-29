# sublime-packages
sublime_packages bak
# install package control
```
import urllib.request,os;
pf = 'Package Control.sublime-package'; 
ipp = sublime.installed_packages_path(); 
urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler())); 
open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```
# sublime license
```
Alexey Plutalov
Single User License
EA7E-860776
3DC19CC1 134CDF23 504DC871 2DE5CE55
585DC8A6 253BB0D9 637C87A2 D8D0BA85
AAE574AD BA7D6DA9 2B9773F2 324C5DEF
17830A4E FBCF9D1D 182406E9 F883EA87
E585BBA1 2538C270 E2E857C2 194283CA
7234FF9E D0392F93 1D16E021 F1914917
63909E12 203C0169 3F08FFC8 86D06EA8
73DDAEF0 AC559F30 A6A67947 B60104C6
```

 # 迁移 package, 备份到github
 ```
 插件默认安装的位置是AppData的目录 【C:\Users\用户名\AppData\Roaming\Sublime Text 3\Packages】
 关闭Sublime，找到它的安装路径，新建一个Data的文件夹，把C盘目录下的Packages文件夹删除掉
 再重新打开Sublime ，References-》 Browser Packages 就发现打开的文件夹就是我们新建的Data文件下的Packages
 ```

 # 清空sublime console
 ```
 print('\n' * 50)
 ```

# 插件
### htmlhint
```
SublimeLinter-contrib-htmlhint
npm install -g htmlhint
rules 规则使用 .htmlhintrc
```
### csslint
```
SublimeLinter-csslint
npm install -g csslint
使用 sublime-setting 中配置csslint
```
### eshint
* SublimeLinter-eslint
* npm install eslint -g
* npm install babel-eslint --save-dev(用来识别es6语法)
* package.json中加入eslintConfig
```
"eslintConfig": {
  "env": {
    "node": true,
    "browser": true
  },
  "rules": {
    "quotes": [//这个规则可以不使用，很多人单双引号都使用，新的项目可以约定好再使用
      2,
      "single"
    ]
  },
  "parser": "babel-eslint"
}
```
