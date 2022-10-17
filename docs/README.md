# 这是一级标题,不会出现在左边目录
## Headline
wowowowowowowo

> An awesome project.
> 
## hhhh

package AGreeting;


public class AGreeting {
private String name;
private String sex;
private double birthday;
private double height;
private double weight;
private double SleepTime;
private double WakeTime;
AGreeting(String name,String sex,double birthday,double height,double weight,double SleepTime,double WakeTime){
	this.name=name;
	this.sex=sex;
	this.birthday=birthday;
	this.height=height;
	this.weight=weight;
	this.SleepTime=SleepTime;
	this.WakeTime=WakeTime;
	
}

	public void setSex(String sex) {
	this.sex = sex;
}

	public String getSex() {
	return sex;
}

	public void setName(String name) {
	this.name = name;
}

public void setBirthday(double birthday) {
	this.birthday = birthday;
}

public void setHeight(double height) {
	this.height = height;
}

public void setWeight(double weight) {
	this.weight = weight;
}

public void setSleepTime(double sleepTime) {
	SleepTime = sleepTime;
}

public void setWakeTime(double wakeTime) {
	WakeTime = wakeTime;
}

	public String getName() {
	return name;
}

public double getBirthday() {
	return birthday;
}

public double getHeight() {
	return height;
}

public double getWeight() {
	return weight;
}

public double getSleepTime() {
	return SleepTime;
}

public double getWakeTime() {
	return WakeTime;
}


public static  String formatString(double BMI){	
	return String.format("%.2f",BMI);
}


public void BMI(){
	
	String BMIStr;
	double BMI= weight/(height*2);
	 BMIStr=Format.formatString(BMI);
	
	
	if(BMI<18.5){
		System.out.println(name+"的BMI指数为"+BMI+"，属于低于正常体重，请多吃点！"); 
		
	}
	if(BMI>=18.5&&BMI<25){
		System.out.println(name+"的BMI指数为"+BMI+"，属于正常体重，请继续保持！"); 
	}
	if(BMI>=25&&BMI<30){
		System.out.println(name+"的BMI指数为"+BMI+"，属于超重，请注意饮食！"); 
	}
	if(BMI>=30&&BMI<35){
		System.out.println(name+"的BMI指数为"+BMI+"，属于一类肥胖，请注意饮食，少吃点！"); 
	}
	if(BMI>=35&&BMI<40){
		System.out.println(name+"的BMI指数为"+BMI+"，属于二类肥胖，请注意饮食，多运动！"); 
	}
	if(BMI>=40){
		System.out.println(name+"的BMI指数为"+BMI+"，属于三类肥胖，请注意饮食，大量运动！"); 
	}
}
public void SleepAdvise(){
	double sleeptime;
	if(SleepTime>WakeTime){
		 sleeptime=(24-SleepTime)+WakeTime;
	}else{
		sleeptime=WakeTime-SleepTime;
	}
	if(sleeptime<=7){
		System.out.println(name+"的睡眠时间是"+sleeptime+",属于睡眠时间过少！请注意休息！");
	}else{
		System.out.println(name+"的睡眠时间是"+sleeptime+",属于睡眠时间正常！继续保持！");
	}
	
	
}
	
	

}
	




//public class   String(double i){
//	String.format("%.2f", i );
//
//}


package AGreeting;

public class Format {
	 String BMIStr=null;
		public static  String formatString(double i){	
			return String.format("%.2f",i);
		
}
}

##
package AGreeting;

//String.format("%.2f", i );

public class Test {
public static void Advise(AGreeting p){
	if(p.getSex()=="男"){
		p. BMI();
	}else{
		p.SleepAdvise();
	}
}
public static void main(String[] args) {
	
		// TODO Auto-generated method stub
		
//		String strBMI= null;
//		strBMI=formatString(BMI);
		AGreeting p1=new AGreeting("裴志明","男",2003,1.70,62,2.00,7.30);
		AGreeting p2=new AGreeting("肖毅","男",2002,1.78,55,2.00,7.40);
		AGreeting p3=new AGreeting("杨磊波","男",2003,1.68,72,23.00,7.30);
		AGreeting p4=new AGreeting("王子珩","男",2003,1.70,64,2.30,7.30);
		AGreeting p5=new AGreeting("欧阳可欣","女",2003,1.60,45,23.30,7.00);
		Advise(p1);
		Advise(p2);
		Advise(p3);
		Advise(p4);
		Advise(p5);
		
//		public static  String formatString(double i){	
//			return String.format("%.2f",i);
//		}

//		public static void main(String[] args){
//			String = null;
//			strBMI=formatString(BMI);
//		}
		
	}

}
