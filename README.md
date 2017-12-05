alien_invasion
==============
练习项目，"外星人入侵"，源于《Python编程：从入门到实践》

*************************************************
`alien_invasion.exe需与images文件夹保持同一目录`<br>
`alien_invasion.zip(不依赖开发环境)是游戏程序`
*************************************************

使用说明：
--------
    开发环境，游戏直接运行alien_invasion.exe即可，也可在具有Python3环境下运行alien_invasion.py
    使用环境，完整的游戏可直接使用alien_invasion.zip(不依赖开发环境)
    alien_invasion.exe与alien_invasion.zip由pyinstall打包可得。pyinstall可使用pip装，具体安装过程略。


练习环境：
--------
    Python:3.5.2 64位
    pyinstall:3.2.1
    

pyinstall使用：
--------
    pyinstaller -F demo.py
    参数 	含义
    -F 	指定打包后只生成一个exe格式的文件
    -D 	–onedir 创建一个目录，包含exe文件，但会依赖很多文件（默认选项）
    -c 	–console, –nowindowed 使用控制台，无界面(默认选项)
    -w 	–windowed, –noconsole 使用窗口，无控制台
    -p 	添加搜索路径，让其找到对应的库。
    -i 	改变生成程序的icon图标


打包注意事项：
--------
    1.打包有2种方式，第一种是使用'-F'打包成单一的可执行文件，如alien_invasion.exe，此项目需要将
      images文件夹放置在与其同一目录下；第二种是默认使用'-D'方式，如alien_invasion.zip(解压)，
      此项目已将images文件夹放置在正确目录并且压缩生成alien_invasion.zip。
    2.打包的文件与《Python编程：从入门到实践》练习的项目文件有所差异，具体为
       (1).ship.py与alien.py中使用的图片设置做了改动,由
            'images/alien.bmp'=>'./images/alien.bmp'
       (2).button.py与scoreboard.py中的字体做了改动,由
            'pygame.font.SysFont(None, 48)'=>'pygame.font.SysFont('arial', 24)'
    3.使用pyinstaller打包时，不会自动包含图片文件，所以最简单的方式是打包后将图片放在运行程序的
      相应路径下。
