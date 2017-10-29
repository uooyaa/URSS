#基于分布式服务（RPC以及微服务）的应用框架
##URSS uooyaa-shareservice
##@since20170828
 
#URSS目标
    JAVA企业应用颇具柔性的共享服务开源框架 
    开发人员只要写业务
    所有微服务、分布式服务、RPC、共享服务、SOA的好处以及相关管理都可以柔性扩充
    扩充的基础基于目前存量IT基础资产
    
#URSS解决的问题
    coming soon
    
    
#URSS适合人群
    coming soon

#URSS包含模块

## urss-tool
    包含部署在windows和linux平台上的多集群一键更新工具
    包含代码生成工具
    urss-tool-maven-appserver  (生成可直接执行并可以配置为windows或者linux服务的应用）
    urss-tool-tomcat(经过定制 适配微服务的tomcat)         
    
## usrr-common-sdk
    公共类
##urss-data

    通用RDBS数据访问门面
    urss-data-api
    urss-data-core
    通用RDBS数据
    urss-data-sqlserver
    urss-data-oracle
    urss-data-mysql    
    urss-data-tidb
    urss-data-elt
    通用缓存以及nosql等
    urss-data-mongodb
    urss-data-redis
    urss-data-hbase
    urss-data-memcache
   
    通用文件等
    urss-data-file

    高性能相关处理
    urss-data-mycat
    urss-data-sharding-jdbc
    urss-data-alirdrs
    
            
            
    
##urss-finder
     监控、追踪、日志分析等
##urss-micros-service
     通用微服务门面
     urss-micro-service-api
     urss-micro-service-core
     urss-rpc-transport(引用urss-transport)   
     urss-micro-service-starter
     
     不同实现
     urss-micro-service-springcloud
     urss-micro-service-dubbox
     urss-micro-service-servicecomb
     urss-micro-service-edas
     urss-micro-service-grpc
              
     会引用urss-rpc应用中内容，替换以上某些模块底层实现
     
##urss-rpc
    通用rpc门面
    urss-rpc-api
    urss-rpc-core
    urss-rpc-io
    urss-rpc-server-publish
    urss-rpc-client-discvery               
    urss-rpc-transport(引用urss-transport)    
    
    rcp核心实现实现    
    urss-rpc-netty      
    urss-rpc-http
    urss-rpc-mina
    urss-rpc-thrift
       
    urss-rpc-zk
    urss-rpc-redis
    urss-rpc-file
    
  
    
##urss-transport
    网络传输通用约定（URSS协议）
    基于企业本身需求生成约定代码并关联版本号
    支持json、xml等通用HTTP层传输
    支持TCP层传输
    支持更多未来好开源传输框架的融入
    URSS协议可以过滤掉非法访问 
    URSS协议可以无侵入生成高质量日志
    
    urss-transport-api            
    urss-transport-core
    urss-transport-serialize
    urss-transport-text            
          

##urss-logging
    通用日志门面
    urss-logging-api
    urss-logging-core
    
    具体实现
    urss-logging-logback-file
    urss-logging-logback-console
    urss-logging-logback-mongodb
    urss-logging-elk
    
    以上不需要重复造轮子，出了部分需要从零开始写外，可以使用sl4j以及log4j2的实现
    但是对外暴露出接口一定要走日志门面，方便后续扩充
    
##urss-message
  通用消息门面
    urss-message-api
    urss-message-core
  
  消息具体实现(消息、队列等)
    urss-message-jdknative
    urss-message-amq
    urss-message-rocketmq
    urss-message-rabbitmq
    urss-message-kafka 
    urss-message-esb-sappx
    urss-message-esb-oraweblogicjms
    urss-message-esb-ibmmq
       
 ##urss-transaction-x
    通用分布式事务门面        
     urss-transaction-x-api
     urss-transaction-x-core
     
     urss-transaction-x-tcc
     urss-transaction-x-edas-gts
     urss-transaction-x-ejb3
     urss-transaction-x-spring
              
  ##urss-cache
     通用缓存|池门面
      urss-cache-api
      urss-cache-core
 
      urss-cache-dbpool-druid        
      urss-cache-dbpool-c3p0        
      urss-cache-dbpool-dbcp        
      urss-cache-dbpool-hikaricp       
 
      urss-cache-jvm-simple
      urss-cache-jvm-ehcache
      urss-cache-jvm-redis
      urss-cache-jvm-memcache
         
      urss-cache-jscss-simple
      urss-cache-jscss-cdn
      urss-cache-jscss-cookie
                               
           
      
     
  ##urss-config
    通用配置门面
      urss-config-api
      urss-config-core
                                     
     urss-config-ctrip-simple
     urss-config-ctrip-apollo
     urss-config-sc-config
     urss-config-baidu-disconf 
                                  
   ##urss-exception
   
       通用异常门面    
       urss-exception-api       
       urss-exception-core                                         
                                         