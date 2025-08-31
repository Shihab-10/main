package edu.diu;

import java.util.List;

public class Main {
    public static void main(String[] args) {
        ProductDao dao = new ProductDao();

        // টেবিল তৈরি হবে (না থাকলে)
        dao.createTable();

        // নতুন প্রোডাক্ট insert করো
        Product p1 = new Product("Laptop", 85000.50);
        dao.insertProduct(p1);

        Product p2 = new Product("Phone", 25000.00);
        dao.insertProduct(p2);

        System.out.println("Products inserted successfully!");

        // সব প্রোডাক্ট select করে প্রিন্ট করো
        List<Product> products = dao.selectAll();
        System.out.println("=== Product List ===");
        for (Product p : products) {
            System.out.println(p);
        }
    }
}
