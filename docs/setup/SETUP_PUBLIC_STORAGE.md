## 配置用于存放数据的存储卷
运行机器学习模型训练需要训练代码，数据以及训练结果的输出，需要通过共享存储进行管理，并在模型训练程序中共享。
Kubernetes中提供了PV（数据卷）和PVC（数据卷声明）作为共享存储的描述对象。阿里云在此之上提供CPFS, NAS和OSS的Flexvolume Driver ，可以轻松将阿里云的CPFS, NAS和OSS 等存储服务对接到Kubernetes集群。

我们建议集群管理员创建一个共享的存储池，共享存储会挂载到Notebook的 `/root/public` 目录中，数据科学家通过这个目录，可以相互分享数据，代码和执行结果。 

我们支持多种类型的共享存储：
* [配置NAS存储](./SETUP_NAS.md)
* [配置CPFS存储](./SETUP_CPFS.md)
* 配置自定义类型存储（TODO）
