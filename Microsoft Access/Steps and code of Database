//Step1 import package
import java.sql.*;
public class Main {
    public static void main(String[] args) {
       try
       {
           //Step 2 and Step 3 load the drivers and create the connection
           Connection con = DriverManager.getConnection("jdbc:ucanaccess://D://JDBC/EventsInfo.accdb");
           //Step 4 Create statement
           Statement st = con.createStatement();
           //Step 5 perpare and execute Query
           ResultSet rs =  st.executeQuery("Select * from Events");
           String eid , ename , edate, evenue;
           //step6 process the results
           while (rs.next())
           {
               eid = rs.getString("EventId");
               ename = rs.getString("EventName");
               edate = rs.getString("EventDate");
               evenue = rs.getString("EventVenue");
               System.out.println(eid + " - " + ename + " , " + edate + " , " + evenue);
           }
           //Step 7 close the connection
           con.close();
       }
       catch(SQLException sqe)
       {
           System.out.println(sqe.getMessage());
       }
    }
}
