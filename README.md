# task2
public class Password {

    private String value;
    private int length;

    public Password(String s) {
        this.value = s;
        this.length = s.length();
    }

    
    public int charType(char c) {

      
        if (c >= 'A' && c <= 'Z') {
            return 1;
        }

       
        else if (c >= 'a' && c <= 'z') {
            return 2;
        }

        
        else if (c >= '0' && c <= '9') {
            return 3;
        }

       
        else {
            return 4;
        }
    }

   
    public int passwordStrength() {

        boolean usedUpper = false;
        boolean usedLower = false;
        boolean usedNum = false;
        boolean usedSym = false;

        int score = 0;

        for (int i = 0; i < value.length(); i++) {
            char c = value.charAt(i);
            int type = charType(c);
