# Java - Inheritance & Overriding

```
class Poly {

    private int width;
    private int height;
    
    public Poly(int width, int height) {
    	this.width = width;
    	this.height = height;
    }
    
    public int getWidth() {
        return this.width;
    }
    
    public void setWidth(int width) {
        this.width = width;
    } 
    
    public int getHeight() {
        return this.height;
    }
    
    public void setHeight(int height) {
        this.height = height;
    } 
    
    public double getArea() {
    	return this.width * this.height;
    }

}

class Triangle extends Poly {

	public Triangle(int width, int height) {
		super(width, height);
	}
    
	@Override
	public double getArea() {
		return this.getWidth() * this.getHeight() * 0.5;
	}
    
}

class Circle extends Poly {

	public Circle(int width, int height) {
		super(width, height);
	}
	
	@Override
	public double getArea() {
		return Math.pow(this.getWidth(), 2) * Math.PI;
	}
	 
}

public class Test10 {
	
	public static void main(String[] args) {
		
		Triangle tri = new Triangle(10, 20);
		System.out.println("삼각형 넓이 : " + tri.getArea());
		
		Circle cir = new  Circle(10, 10);
		System.out.println("원 넓이 : " +cir.getArea());
	}

}
```
