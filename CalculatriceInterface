import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.*;
import javax.swing.border.Border;

public class CalculatriceInterface implements ActionListener {
    JFrame guiFrame;
    JPanel buttonPanel;
    JTextField resultLabel;
    // Remove unused variables: int calcOperation = 0;
    // int currentCalc;

    // Fix the instance creation: CalculatriceInterface model = new CalculatriceInterface();
    Calculatrice model = new Calculatrice();

    public CalculatriceInterface() {
        guiFrame = new JFrame();
        guiFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        guiFrame.setTitle("Calculette Graphique");
        guiFrame.setSize(300, 300);
        guiFrame.setLocationRelativeTo(null);
        resultLabel = new JTextField();
        resultLabel.setBackground(Color.BLACK);
        Font font = new Font(Font.SERIF, Font.BOLD, 40);
        resultLabel.setForeground(Color.green);
        resultLabel.setFont(font);
        resultLabel.setHorizontalAlignment(JTextField.LEFT);
        resultLabel.setEditable(false);
        guiFrame.add(resultLabel, BorderLayout.NORTH);
        buttonPanel = new JPanel();
        GridLayout grid = new GridLayout(4, 4);
        buttonPanel.setLayout(grid);
        guiFrame.add(buttonPanel, BorderLayout.CENTER);
        String name[] = {"1", "2", "3", "+", "4", "5", "6", "-", "7", "8", "9", "*", "CE", "0", "=", "/"};
        for (int i = 0; i < name.length; i++) {
            JPanel pan = new JPanel();
            pan.setLayout(new GridLayout(1, 1));
            String nombre = "1234567890";
            if (nombre.toString().toLowerCase().contains(name[i].toLowerCase()))
                pan.setBackground(Color.BLUE);
            else
                pan.setBackground(Color.RED);
            pan.setBorder(BorderFactory.createEmptyBorder(2, 2, 2, 2));
            addButton(pan, name[i]);
            buttonPanel.add(pan);
        }
        guiFrame.setLocationByPlatform(true);
        guiFrame.setVisible(true);
    }

    private void addButton(Container parent, String name) {
        JButton button = new JButton(name);
        button.setActionCommand(name);
        button.addActionListener(this);
        parent.add(button);
    }

    public void actionPerformed(ActionEvent e) {
        // Implement the appuieBouton method in your Calculatrice class
        // model.appuieBouton(e.getActionCommand());

        JButton but = (JButton) e.getSource();
        but.setBorder(null); // Reset the border
        resultLabel.setText(model.getAffichage());
    }

    public static void main(String[] args) {
        EventQueue.invokeLater(new Runnable() {
            public void run() {
                new CalculatriceInterface();
            }
        });
    }
}
