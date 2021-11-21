//# Clock
//I couldn't figure out how to rotate the entire clock 45 degrees to the left so I just made sure that you get a good solid stretch every time that you look at my clock
function setup() {
	createCanvas(800, 800);
}	

	function draw() {
		background(220);
		rect(250, 250, 300, 300);
		fill(1000);

		ellipse(width / 2, height / 2, 250, 250);
		fill(165, 42, 42);
		
		ellipse(width/2,height/2,10,10);
		//stroke(1);
		//	strokeweight(5);
		//rectMode(CENTER);
		angleMode(DEGREES);
		
				strokeWeight(3);
		fill(1);
	//fill(1); //numbers
	textSize(20);
		text('12', 285, 405);
		text('6',500,405);
		text('3',395,295);
		text('9',395,520);
		text('1',305,350);
		text('2',345,310);
		text('4',450,310);
		text('5',490,355);
		text('7',485,460);
		text('8',445,500);
		text('10',335,495);
		text('11',295,455);
		


		translate(width / 2, height / 2);

		push();
		let secHand = map(second(), 0, 59, 0, 359);
		rotate(secHand);
		rect(0, 0, -110, 0);
		pop();

		push();
		let minuteHand = map(minute(), 0, 59, 0, 359);
		rotate(minuteHand);
		rect(0, 0, -80, 1);
		pop();

		push();
		let hourhand = map(hour(), 0, 12, 0, 359);
		rotate(hourhand);
		rect(0, 0, -60, 3);
		pop();



	}
