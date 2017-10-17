tomcat版本号为 7.0.69

1.使用了log4j替换了tomcat本身的logging，log4j的配置文件为lib/log4j.properties，conf/logging.properties.del为删除的logging配置文件

2.在bin/catalina.sh中有以下字符串需要替换:
${superdiamond.host} 使用的superdiamond host
${superdiamond.projcode} 使用的superdiamond工程名
${profile.active} 使用的superdiamond profile
${server.name} 服务名称，用于生成pid文件

3.在conf/server.xml中有以下字符串需要替换
${server.port} 服务端口
${server.shutdown.port} 关闭服务使用的端口
${server.redirect.port} SSL的redirectPort端口

4.sso如需使用redis保存共享session请自行修改配置
