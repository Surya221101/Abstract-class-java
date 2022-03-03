# Abstract-class-java
//I have created a abstract class instrument whose abstract method is overrided by 3 child classes ,its an very intresting code, do check it out
package exceptionnabstract;
abstract class Instrument{
	abstract void play();
}
class Piano extends Instrument{
	
	@Override
	void play() {
		System.out.println("Piano is playing");
	}
}
class Flute extends Instrument{
	@Override
	void play() {
		System.out.println("Flute is playing");	
	}
}
class Guitar extends Instrument{
	@Override
	void play() {
		System.out.println("Guitar is playing");	
	}
}
public class Demo7 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Instrument a[]=new Instrument[10];
		for(int i=0;i<10;i++) {
			switch(i%3) {
			case 0:{a[i]=new Piano();
			break;}
			case 1:{a[i]=new Flute();
			break;}
			case 2:{a[i]=new Guitar();
			break;}
			}
		}
		for(int i=0;i<10;i++) {
			System.out.println("array index="+(i+1));
			if(a[i] instanceof Piano) {
				System.out.println("Object of Piano");
			}
			if(a[i] instanceof Flute) {
				System.out.println("Object of Flute");
			}
			if(a[i] instanceof Guitar) {
				System.out.println("Object of Guitar");
			}
			a[i].play();
		}
	}

}
