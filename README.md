# Rysunek

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
