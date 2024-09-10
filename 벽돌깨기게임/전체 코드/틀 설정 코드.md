GameFrame.java
    
    package main;
    
    import javax.swing.JFrame;
    
    public class GameFrame extends JFrame {
    
        public GameFrame() {
            this.setTitle("Brick Breaker Game");
            this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
            this.setSize(700, 600);  // 창 크기 설정
            this.setResizable(false);  // 창 크기 변경 불가
            this.add(new GamePanel());  // GamePanel을 추가
            this.setVisible(true);  // 창을 표시
        }
    
        public static void main(String[] args) {
            new GameFrame();  // 게임 시작
        }
    }
