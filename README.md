# bank-system
package test;

import java.util.Scanner;

public class Test {
    
    public static void main(String[] args)
    {
      Acount a1=new Acount(), a2=new Acount(),a3=new Acount();
      
      a1.insert(4451238, "kerols" , 10000);
      a1.deposit(12000);
      a1.withdrw(2000);
      a1.chekBalance();
      a1.toString();
        
      a2.insert(9563145, "nagy" , 100);
      a2.deposit(50);
      a2.withdrw(140);
      a2.chekBalance();
      a2.toString();
      
      a3.insert(4451238, "Azmy" , 500);
      a3.deposit(550);
      a3.withdrw(10);
      a3.chekBalance();
      a3.toString();        
    
    }
}




/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test;

/**
 *
 * @author TheGenius
 */
public class Acount {
    private int accoountNo;
    private String name;
    private float amount;
    
    public void insert(int a,String n, float amt){
        this.accoountNo = a;
        this.name = n;
        this.amount = amt;
    }
    
    public void deposit(float amt){
        this.amount = this.amount + amt;
        System.out.println(amt + "depoited");
    }
    
    public void withdrw(float amt)
    {
        if(amount<amt){
            System.out.println("Insufficient Balance");
        }
        else
        {
            this.amount = this.amount-amt;
            System.out.println(amt + "withdrawn");
        }
    }
    
    public void chekBalance()
    {
        System.out.println("Balance = " + this.amount);    
    }

    @Override
    public String toString() {
        return "Acount{" + "accoountNo=" + accoountNo + ", name=" + name + ", amount=" + amount + '}';
    }
    
    
    
}
