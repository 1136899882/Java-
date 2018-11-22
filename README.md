使用通配符
在执行SQL对象之前，必须调用相应的方法设置通配符？代表具体的值
如： sql.setFloat(1,1.76f);
     sql.setString()
     
     
     
     
     
     
     
     String str = "select * from mess where height < ? and name = ?"
     PreparedStatement sql = con.prepareStatement(str);
     
     
