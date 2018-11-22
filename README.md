使用通配符
在执行SQL对象之前，必须调用相应的方法设置通配符？代表具体的值
如： sql.setFloat(1,1.76f);
     sql.setString()
     
     
     
     
     
     
     
     String str = "select * from mess where height < ? and name = ?"
     PreparedStatement sql = con.prepareStatement(str);
     
     
     
     随即流
      使用RandomAccessFile类来创建一个随机访问的文件流，创建的流指向既可以作为源也可以作为目的地
       构造方法
       
       
       
       try{ inAndOut = new RandomAccessFile("","rw");
       for(int i =0; i<data.length;i++){
       }
       }
       
     
