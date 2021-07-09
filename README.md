# HITDAY30

package hit.day30;
import java.util.Enumeration;
import java.util.Iterator;
import java.util.Map;
import java.util.Properties;
import java.util.Set;
public class PropRevision {
	public static void main(String[] args) {
		Properties prop=new Properties();
		
		prop.put("mykey1", "myvalue111111111111");
		prop.put("mykey2", "value 22222222222222222");
		prop.put("mykey3", "value 22222222222222222");
		
		//First Reading method
		System.out.println(prop.get("mykey1"));
		System.out.println("++++++++++++++++++++++++++++++++++++++++");
		//Second Reading Method
		Enumeration e=prop.elements();
		while(e.hasMoreElements()) {
			System.out.println(e.nextElement());
		}
		
		System.out.println("++++++++++++++++++++++++++++++++++++++++");
		
		Set set=prop.entrySet();
		Iterator iter=set.iterator();
		while(iter.hasNext()) {
			Map.Entry me=(Map.Entry)iter.next();
			System.out.println(me.getKey()+":"+me.getValue());
		}
	}
}

package hit.day30;
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;
import java.util.TreeMap;
public class ColDemo7 {
	public static void main(String[] args) {
		//Map<String,String> map=new HashMap<>();
		Map<String,String> map=new TreeMap<>((obj1,obj2)->{return obj2.compareTo(obj1);});
		
		map.put("mykey1", "my value 11111111111");
		map.put("mykey2", "my value 22222222222");
		map.put("mykey3", "my value 33333333333");
		System.out.println(map);
		
		System.out.println(map.get("mykey1"));
		
		Set<Map.Entry<String,String>> set= map.entrySet();
		
		Iterator<Map.Entry<String,String>> iter=set.iterator();
		while(iter.hasNext()) {
			Map.Entry<String,String> me=iter.next();
			System.out.println(me.getKey()+":"+me.getValue());
		}
		
	}
}

package hit.day6;
public class ArrayDemo {
	public static void main(String[] args) {
		
		//Normally variables can store only one value..
		//but arrays can store more than 1 value...
		
	//	int marks[]= {90,83,85};//single dimensional array with initialization
		
		int marks[]=new int[3];//single dimensional array without initialization -3 is size of array
		marks[0]=90;//array index always starts with zero
		marks[1]=83;
		marks[2]=85;
		
		for(int i=0;i<marks.length;i++) {//marks.length will get you the size of the array
			System.out.println(marks[i]);
		}
	}
}
