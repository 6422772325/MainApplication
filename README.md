// MainApp.java

import org.hibernate.Session;
import org.hibernate.Transaction;

public class MainApp {
    public static void main(String[] args) {

        try (Session session = HibernateUtil.getSessionFactory().openSession()) {
            Transaction tx = session.beginTransaction();

            // === DATABASE 1: AUTHOR - BOOK ===
            // TODO: Create Author and 2 Book objects
            // Link books to author
            // session.persist(author);

            // === DATABASE 2: STUDENT - COURSE - ENROLLMENT ===
            // TODO: Create Student, Course, Enrollment
            // Link enrollment to student and course
            // session.persist(student);

            // === DATABASE 3: USER - PROFILE ===
            // TODO: Create User and Profile objects
            // Link profile to user
            // session.persist(user);

            tx.commit();
            System.out.println("✅ Data inserted successfully.");
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
