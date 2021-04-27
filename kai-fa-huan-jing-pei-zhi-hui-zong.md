# dev-environment

## zsh: command not found: mvn 

如果已经配置了maven，但是每次在终端执行 **mvn** 命令的时候，都必须要执行下 **source ~/.bash\_profile** 才能生效。这是因为当 Mac 上安装了 **zsh** 后，**.bash\_profile** 文件的配置无法生效。解决方案是：

```bash
echo "source ~/.bash_profile" > ~/.zshrc
```

当 **zsh** 启动的时候，会读取 **.bash\_profile** 文件的内容并使之生效。





## Have you had a chance to answer the previous question?

Yes, after a few months we finally found the answer. Sadly, Mike is on vacations right now so I'm afraid we are not able to provide the answer at this point.



