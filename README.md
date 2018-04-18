# knowledges
knowledge of personal
personal records
some command of git
git diff --name-status master...branchname(>changed-files.diff)  get a changed log of the branch diff master

git reset --hard commit-id     reset to any commit
git reset --hard:              reset last commit
git reset --hard HEAD~3        reset 3 last commit

#本地到远程scp
scp -r local files user@ip:/remote path
#远程到本地scp
scp user@ip:/remote path/files local path/files

#vim 全部替换
:%s/text/totext/g

#mysql 新增实例
1. 创建data目录 cnf 文件
2. 执行mysql初始化
mysql/scripts/mysql_install_db --basedir=/mysqldir/ --datadir=/实例数据文件夹路径 --defaults-file=/实例.cnf文件
/mysqlpath/bin/mysql -S /实例datapath/run/mysql.sock  #指定实例访问

#shell 按行读取文件
dirname=$1'dirname'
#$1 shell 传参读取
name ='fileslist.txt'
rm -rf $dirname
mkdir -p $dirname
sed 's/^[ \t\r]*//; s/[ \t\r]*$//' $name | while read LINE
do
  namesize = ${#LINE}
    if [[ $namesize -lt 1 || 'echo $LINE | grep "#"' ]]
    then
      echo"遇到#字符的操作"
    else
      filepath = $(dirname "$LINE")
      mkdir -p "$dirname/$filePath"
      if [ -d "$path/$LINE" ]
        then
          COMMAND = "cp -R $path/$LINE  $dirname/$LINE"
        else
          COMMAND = "cp $path/$LINE  $dirname/$LINE"
       fi
       $COMMAND
     fi
 done



#php 完整configure
./configure --prefix=/usr/local/php --with-config-file-path=/usr/local/php/etc --with-config-file-scan-dir=/etc/php --with-mysql=mysqlnd --with-mysqli=mysqlnd --with-pdo-mysql=mysqlnd --with-zlib --with-bz2 --with-gd --with-png-dir --with-jpeg-dir --with-freetype-dir --enable-gd-native-ttf --with-iconv --enable-xml --enable-bcmath --enable-shmop --enable-sysvsem --enable-inline-optimization --enable-mbregex --enable-fpm --enable-mbstring --with-openssl --enable-pcntl --enable-sockets --with-xmlrpc --enable-zip --enable-soap --without-pear --enable-session --with-mrrypt --with-curl --enable-ftp
