# docker安裝

使用 yum install docker 直接安裝

![image-20200805172945530](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805172945530.png)

![image-20200805173020938](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805173020938.png)

![image-20200805173040378](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805173040378.png)

查看docker的版本  docker --version

![image-20200805173210409](C:\Users\19074\AppData\Roaming\Typora\typora-user-images\image-20200805173210409.png)



設置開機啟動docker進程

```
systemctl start docker.service
systemctl enable docker.service
```