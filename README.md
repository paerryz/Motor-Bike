# Motor-Bike

------------------------------------------------------
package parrynguyen.motorbike;

public class MotorBike {
	// state
	private int speed; // member variable

	MotorBike() {
		this(5);
	}

	MotorBike(int speed) {
		this.speed = speed;
	}

	public int getSpeed() {
		return speed;
	}

	public void setSpeed(int speed) {
		if (speed > 0) {
			this.speed = speed;
		}
	}

	public void increaseSpeed(int howMuch) {
		setSpeed(this.speed + howMuch);
	}

	public void decreaseSpeed(int howMuch) {
		setSpeed(this.speed - howMuch);
	}

	void start() {
		System.out.println("Bike Start");
	}
}

-------------------------------------------------
#Motor Bike Runner: 


package parrynguyen.motorbike;

public class MotorBikeRunner {

	public static void main(String[] args) {
		MotorBike ducati = new MotorBike(100);
		MotorBike honda = new MotorBike(200);

		MotorBike somethingElse = new MotorBike();

		System.out.println(ducati.getSpeed());

		System.out.println(honda.getSpeed());
		System.out.println(somethingElse.getSpeed());

		ducati.start();
		honda.start();

		// ducati.setSpeed(100);

//		ducati.increaseSpeed(100);
//		honda.increaseSpeed(100);
//
//		ducati.decreaseSpeed(50);
//		honda.decreaseSpeed(50);

//		int ducatiSpeed = ducati.getSpeed();
//		ducatiSpeed = ducatiSpeed + 100;
//		ducati.setSpeed(ducatiSpeed);



	}

}
