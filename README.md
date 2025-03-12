interface Runnable
{
    void display();
}
class Computer
{
    void cpu(){
        System.out.println("Member Inner Class");
    }
    class Processor
    {
        void process()
        {
            System.out.println("Member Inner Class");
        }
    }
}
class Anonymous implements Runnable
{
    @Override
    public void display()
    {
        System.out.println("Anonymous class override from interface Runnable");
    }
}
class innerClass 
{
  public static void main (String[] args) {
        Computer c=new Computer();
        c.cpu();
        Computer.Processor p=c.new Processor();
        p.process();
        Runnable r=new Runnable()
        {
            @Override
            void display()
            {
                System.out.println("Anonymous class executed.....");
            }
        };
        r.display();
        Anonymous a= new Anonymous();
        a.display();
        
    }
}
