# 識別hfs

第一步：

rpm --import http://elrepo.org/RPM-GPG-KEY-elrepo.org

第二步：（更换了资源）

rpm -Uvh http://www.elrepo.org/elrepo-release-7.0-2.el7.elrepo.noarch.rpm
第三步：
yum install kmod-hfsplus
--------------------- 
