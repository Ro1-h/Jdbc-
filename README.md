# Jdbc-
package jdbccom.db;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;

public class jdbc { 
	public static void main(String args[]) {
		
		try {
			//step1
			Class.forName("com.mysql.cj.jdbc.Driver");
			
			//step2
			Connection conn=DriverManager.getConnection("jdbc:mysql://localhost:0011/jdbc","root","tyu@");
			//System.out.println(conn);
			
			//step3
			PreparedStatement ps=conn.prepareStatement("insert into jdbc_tb(id,name,roll,address) values('2172','nuji','1610','India11' )");
			
			//step4
			ps.execute();
			System.out.println("Data insert Sucessfully");
			//step5
			conn.close();
			
		} catch (Exception e) {
			// TODO Auto-generated catch block
			e.printStackTrace();;
		}
	}

}
