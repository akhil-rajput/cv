# cv
/******************************************************************************

Welcome to GDB Online.
GDB online is an online compiler and debugger tool for C, C++, Python, Java, PHP, Ruby, Perl,
C#, VB, Swift, Pascal, Fortran, Haskell, Objective-C, Assembly, HTML, CSS, JS, SQLite, Prolog.
Code, Compile, Run and Debug online from anywhere in world.

*******************************************************************************/
public class Main
{
	public static void main(String[] args) {
	    String s="aabbcccbad";
	    StringBuilder str=new StringBuilder("");
	    int k=3;
	    str.append(s);
	   boolean flag=true;
	   
	    while(flag){
	        int count=1;
	        String res="";
	        flag=false;
	        
	        for(int i=0;i<str.length()-1;i++){
	            if(str.charAt(i)==str.charAt(i+1)){
	                count++;
	               
	                if(count==k){
	                     int j=0;
	                    for( j=0;j<i-1;j++){
	                        flag=true;
	                        
	                        res+=str.charAt(j);
	                        
	                    }
	                     i++;
	                     
	                    String sub=str.substring(i+1,str.length());
	                    
	                    str.delete(0,str.length());
	                    str.append(res);
	                    str.append(sub);
	                    System.out.println(str);
	                    res="";
	                    count=1;
	                    	
	                }
	            }
	            else{
	                count=1;
	            }
	        }
	    
	   
	    }   
	
	}
}
******************************************///////Cut m and n letters from the end of the string, then find the number of turns to get back the original string//////////////////////////////////////


public class Main
{
	public static void main(String[] args) {
	    String s="arya";
	    int count=0;
	    boolean flag=true;
	    int m=1;
	    int n=2;
	    StringBuilder str=new StringBuilder("");
	    str.append(s);
	    while(flag){
	       String str1=str.substring(str.length()-m, str.length());
	       String str2=str.substring(str.length()-(m+n), str.length()-m);
	       String str3=str.substring(0, str.length()-(m+n));
	       str.delete(0,str.length());
	         str.append(str2);
	       str.append(str1);
	     
	       str.append(str3);
	       System.out.println(str);
	       count++;
	       if(str.toString().equals(s)){
	           
	          flag=false; 
	       }
	    }
		System.out.println(count);
	}
}

