public class UserThread Example {

    public static void main(String[] args) {

        Thread userThread = new Thread(() -> {

           for (int i = 1; i <= 5; i++) {

               System.out.println("User Thread - Count: " + i);

               try {

                   Thread.sleep(1000);

                } catch (InterruptedException e) {

                e.printStackTrace();

                }

             }

          });

           userThread.start();

           // Main thread continues executing

             for (int i = 1; i <= 3; i++) {

                System.out.println("Main Thread - Count: " + i);

                try {

                   Thread.sleep(500);

                } catch (InterruptedException e) {

                e.printStackTrace();

                }

            }

}
