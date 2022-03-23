## SHapeTester


# Main
import java.util.Scanner; 
public class Main{
  public static void main(String[] args) {
    Scanner scan = new Scanner(System.in);
    Box b1 = new Box();
    Sphere s1 = new Sphere();
    Pyramid p1 = new Pyramid();
System.out.println("Welcome to shape tester");
System.out.println("Enter box length");
int val = scan.nextInt();
System.out.println("Enter box width");
  val = scan.nextInt();
System.out.println("Enter box height");
  val = scan.nextInt();
b1.setL(val);
b1.setH(val);
b1.setW(val);
System.out.println("Volume: " + b1.calcVol()); 
System.out.println("Surface Area: " + b1.calcSurfArea());   
System.out.println("Enter sphere radius: ");
  int valu = scan.nextInt();
    s1.setR(valu);
    System.out.println("Volume: " + s1.calcVol()); 
    System.out.println("Surface Area: " + s1.calcSurfArea());
System.out.println("Enter pyramid length: ");
  int value = scan.nextInt();
System.out.println("Enter pyramid width: ");
  value = scan.nextInt(); 
System.out.println("Enter pyramid height: ");
  value = scan.nextInt(); 
    p1.setL(value);
    p1.setH(value);
    p1.setW(value);
    System.out.println("Volume: " + p1.calcVol()); 
    System.out.println("Surface Area: " + p1.calcSurfArea());
  }
}


# Box 
public class Box{
  private int l;
  private int w;
  private int h;
  public Box() {
    l = 0;
    w = 0;
    h = 0; 
  }
  public void setL(int l) {
    this.l = l;
  }
  public void setH(int h) {
    this.h = h;
  }
  public void setW(int w) {
    this.w = w;
  }
  public int calcVol(){
    int vol = l*w*h;
    return vol;
  }
  public int calcSurfArea() {
    int sa = 2 * (l * 2 + l * h + w * h);
    return sa; 
  }
}


# Sphere 
public class Sphere{
  private int r;
  private int h;
  public Sphere() {
    r = 0;
    h = 0; 
  }
  public void setR(int r) {
    this.r = r;
  }
  public void setH(int h) {
    this.h = h;
  }
  public int calcVol(){
    int vol = 4/3 * 3 * (r * r * r); 
    return vol;
  }
  public int calcSurfArea() {
    int sa = 4 * 3 * (r * r);
    return sa; 
  }
}


# Pyramid  
public class Pyramid{
  private int l;
  private int w;
  private int h;
  public Pyramid() {
    l = 0;
    w = 0;
    h = 0; 
  }
  public void setL(int l) {
    this.l = l;
  }
  public void setW(int w) {
    this.w = w;
  }
  public void setH(int h) {
    this.h = h;
  }
  public int calcVol(){
    int vol = 1/3 * (l * w * h);
    return vol;
  }
  public int calcSurfArea() { 
    int sa = 2/3 * (l * 2 + l * h + w * h);
    return sa; 
  }
}
