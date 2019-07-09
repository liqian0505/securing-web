# securing-web学习记录
## 看文档
* 用时约0.5小时 [官方地址](https://spring.io/guides/gs/securing-web/)
## 写代码并运行
* 用时约2小时
## 总结
* WebSecurityConfig class extends WebSecurityConfigurerAdapter and overrides a couple of its methods 
to set some specifics of the web security configuration.
  + WebSecurityConfig 这个类重写方法做了一些安全性设置
  + configure(HttpSecurity)方法定义哪些url需要验证，哪些不需要，还指定了一个登录页
```
　　 .authorizeRequests()
        .antMatchers("/", "/home").permitAll()
        .anyRequest().authenticated()
        .and()
     .formLogin()
         .loginPage("/login").permitAll()
```
