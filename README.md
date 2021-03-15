# Rysunek

// Moim rysunkiem 2D będzie niebieski latawiec.


package rysunek;

import java.awt.EventQueue;
import java.awt.Color;
import java.awt.Graphics;
import java.awt.Graphics2D;
import javax.swing.JFrame;
import javax.swing.JPanel;

class Surface extends JPanel {

    private void doDrawing(Graphics g) {
        
        Graphics2D g2d = (Graphics2D) g.create();
        
// rysowanie dwóch linii:
// jedna pionowa-dłuższa: 

        g2d.setPaint(Color.blue);
        g2d.drawLine(120, 5, 120, 230);
        
// druga pozioma-krótsza: 

        g2d.setPaint(Color.blue);
        g2d.drawLine(40, 70, 200, 70);
       
// łączenie linii w trójkąty: dwa mniejsze i dwa większe:
      
        g2d.setPaint(Color.blue);
        g2d.drawLine(120, 5, 40, 70);    
        g2d.setPaint(Color.blue);
        g2d.drawLine(120, 5, 200, 70);
        g2d.setPaint(Color.blue);
        g2d.drawLine(40, 70, 120, 230);
        g2d.setPaint(Color.blue);
        g2d.drawLine(200, 70, 120, 230);
        
// narysowanie czerwonej linii, czyli sznurka, za który można trzymać latawiec:
            
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


![Zrzut ekranu (358)](https://user-images.githubusercontent.com/80594097/111124389-c30a5e00-8570-11eb-8d14-71f67b09a86f.png)



