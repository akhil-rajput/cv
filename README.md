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
