#### activiti hello world
        ProcessEngine engine = ProcessEngines.getDefaultProcessEngine();
        //存储服务
        RepositoryService rs = engine.getRepositoryService() ;

        //运行时服务
        RuntimeService runtimeService = engine.getRuntimeService() ;

        //任务服务

        TaskService taskService = engine.getTaskService() ;


        rs.createDeployment().addClasspathResource("first.bpmn").deploy();

        ProcessInstance instance = runtimeService.startProcessInstanceByKey("myProcess_1");

        org.activiti.engine.task.Task t = taskService.createTaskQuery().processInstanceId(instance.getId()).singleResult();
        System.out.println("tname :"+t.getName());
        taskService.complete(t.getId());

        t = taskService.createTaskQuery().processInstanceId(instance.getId()).singleResult();
        System.out.println("tname :"+t.getName());
        taskService.complete(t.getId());


        t = taskService.createTaskQuery().processInstanceId(instance.getId()).singleResult();
        System.out.println("task :"+t);

        engine.close();
        
  #### activiti 数据库表概览
      ACT_GE genernal 保存通用数据  资源数据
          流程文件、流程图 （rev 版本）
      ACT_RE Repository 存储表 流程定义、流程部署信息
          ACT_RE_PROCDEF 流程定义
      ACT_ID identity 身份数据表 用户 用户用户组
          ACT_ID_INFO 用户信息key:value表 (type account 用户账号/userinfo 用户信息/null)  且使用parentid自关联
      ACT_RU runtime 运行时的表 
          TASK 
          RU_JOB
          SUPENDED_JOB
          TIMER_JOB
          DEADLETTER_JOB       
      ACT_HI history 历史数据表
          各种历史数据表
      ACT_DMN 规则引擎数据表
