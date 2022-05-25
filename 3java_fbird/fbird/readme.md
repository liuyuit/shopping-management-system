# readme

## references

> [zhanglei-workspace](https://github.com/zhanglei-workspace)/**[shopping-management-system](https://github.com/zhanglei-workspace/shopping-management-system)**

## sql

<details>
<summary>goods</summary>
    CREATE TABLE `goods` (
  `G_ID` int(11) NOT NULL AUTO_INCREMENT,
  `G_NAME` varchar(50) NOT NULL DEFAULT '',
  `G_DESCRIBE` varchar(255) NOT NULL DEFAULT '',
  `G_PRICE` decimal(10,2) NOT NULL DEFAULT '0.00',
  `G_MADE` varchar(255) NOT NULL DEFAULT '',
  `G_AMOUNT` int(10) NOT NULL DEFAULT '0',
  `G_CREATE_DATE` timestamp NULL DEFAULT CURRENT_TIMESTAMP,
  `G_PIC` varchar(255) NOT NULL DEFAULT '',
  PRIMARY KEY (`G_ID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
</details>

<details>
    <summary>u_user</summary>
CREATE TABLE `u_user` (
  `U_ID` int(10) NOT NULL AUTO_INCREMENT COMMENT '用户id',
  `U_NAME` varchar(255) NOT NULL DEFAULT '' COMMENT '用户名',
  `U_NICK_NAME` varchar(255) NOT NULL DEFAULT '',
  `U_SEX` tinyint(2) NOT NULL DEFAULT '1' COMMENT '0:女  1:男',
  `U_PASSWORD` varchar(255) NOT NULL DEFAULT '' COMMENT '密码',
  `U_EMAIL` varchar(255) NOT NULL DEFAULT '' COMMENT '邮箱',
  `U_STATE` tinyint(2) NOT NULL DEFAULT '2' COMMENT '-2:未启用  2:启用',
  `U_IS_SELLER` tinyint(2) NOT NULL DEFAULT '-3' COMMENT '-3:非卖家  3:卖家',
  `U_LAST_LOGIN_TIME` timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT '最后登录时间',
  `U_CREATE_DATE` timestamp NULL DEFAULT CURRENT_TIMESTAMP COMMENT '创建日期',
  PRIMARY KEY (`U_ID`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4;
</details>



## run

右侧 maven -> mvn clean -> mvn package