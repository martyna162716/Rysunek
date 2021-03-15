# Rysunek


package rysunek;

/**
 *
 * @author Martyna
 */
 
import java.awt.EventQueue;
import java.awt.Color;
import java.awt.Graphics;
import java.awt.Graphics2D;
import javax.swing.JFrame;
import javax.swing.JPanel;

class Surface extends JPanel {

    private void doDrawing(Graphics g) {
        
        Graphics2D g2d = (Graphics2D) g.create();
        
        g2d.setPaint(Color.blue);
        g2d.drawLine(120, 5, 120, 230);
       
        g2d.setPaint(Color.blue);
        g2d.drawLine(40, 70, 200, 70);
      
        g2d.setPaint(Color.blue);
        g2d.drawLine(120, 5, 40, 70);    
        g2d.setPaint(Color.blue);
        g2d.drawLine(120, 5, 200, 70);
        g2d.setPaint(Color.blue);
        g2d.drawLine(40, 70, 120, 230);
        g2d.setPaint(Color.blue);
        g2d.drawLine(200, 70, 120, 230);
          
        g2d.setPaint(Color.red);
        g2d.drawLine(120, 230, 120, 290);
            
        g2d.dispose();
     
    }

    @Override
    public void paintComponent(Graphics g) {
        
        super.paintComponent(g);
        doDrawing(g);
    }
}

public class GradientsEx extends JFrame {
    
    public GradientsEx() {

        initUI();
    }    
    
    private void initUI() {
        
        add(new Surface());
        
        setTitle("Gradients");
        setSize(350, 350);
        setLocationRelativeTo(null);            
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
    
    public static void main(String[] args) {

        EventQueue.invokeLater(() -> {
            GradientsEx ex = new GradientsEx();
            ex.setVisible(true);
        });
    }    
}



// Moim rysunkiem 2D jest niebieski latawiec. Rysunek zaczynam od narysowania dwóch linii: poziomej-krótszej i pionowej-dłuższej. Linie te są prostopadłe. Następnie linie te łączę ze sobą w taki sposób, że powstają 4 trójkąty prostokątne, dwa mniejsze i dwa większe. Na sam koniec dorysowuję czerwoną linię, czyli sznurek, za który można trzymać latawiec.

![Zrzut ekranu (359)](https://user-images.githubusercontent.com/80594097/111125171-9d318900-8571-11eb-87f0-4c768449cc66.png)


