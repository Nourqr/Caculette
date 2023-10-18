public class Calculatrice {
    private String affichage;

    public Calculatrice() {
        this.affichage = "0";
    }

    public void appuieBouton(String button) {
        // Implement the logic to update the calculation based on the button pressed
        // For simplicity, let's say pressing a number button appends the number to the display
        if (button.matches("[0-9]")) {
            affichage += button;
        } else if (button.equals("=")) {
            // Implement the logic to perform the calculation when "=" is pressed
            // For simplicity, let's say the result is the same as the current display
        } else if (button.equals("CE")) {
            // Implement the logic to clear the display
            affichage = "0";
        } else {
            // Handle other operators or buttons
        }
    }

    public String getAffichage() {
        return affichage;
    }
}
