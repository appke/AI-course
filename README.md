# AI-course
AI课程课件

- [使用LFS解决GitHub无法上传大文件问题 | qhh.me](https://qhh.me/2018/01/20/%E4%BD%BF%E7%94%A8LFS%E8%A7%A3%E5%86%B3GitHub%E6%97%A0%E6%B3%95%E4%B8%8A%E4%BC%A0%E5%A4%A7%E6%96%87%E4%BB%B6%E9%97%AE%E9%A2%98/)

```
brew install git-lfs
git lfs install
# 自动生成.gitattributes文件
git lfs track "*.pdf"
git add .gitattributes

git commit -m "Updated the attributes"
git push origin master
```



```
# 增加追踪大文件
*.pdf filter=lfs diff=lfs merge=lfs -text
*.csv filter=lfs diff=lfs merge=lfs -text

# 查看追踪的大文件
git lfs ls-files
```





```
remote: error: File 1124-Ensemble Learning（1）/sf_data/train.csv is 121.53 MB; this exceeds GitHub's file size limit of 100.00 MB
remote: warning: File 1124-Ensemble Learning（1）/sf_data/test.csv is 86.78 MB; this is larger than GitHub's recommended maximum file size of 50.00 MB
```

