## MapGenerator.java

    package main;
    
    import java.awt.BasicStroke;
    import java.awt.Color;
    import java.awt.Graphics2D;
    
    public class MapGenerator {
    public int[][] map;   // 벽돌의 상태를 저장하는 2차원 배열
    public int brickWidth;  // 각 벽돌의 너비
    public int brickHeight;  // 각 벽돌의 높이

    // 생성자: 행과 열의 개수에 따라 벽돌 배열을 초기화
    public MapGenerator(int row, int col) {
        map = new int[row][col];  // row x col 크기의 2차원 배열 생성
        for (int i = 0; i < map.length; i++) {
            for (int j = 0; j < map[0].length; j++) {
                map[i][j] = 1;  // 배열의 각 위치를 1로 설정하여 벽돌이 존재함을 나타냄
            }
        }
        // 벽돌의 너비와 높이를 설정 (각 행, 열에 맞게 크기 조정)
        brickWidth = 540 / col;
        brickHeight = 150 / row;
    }

    // 벽돌을 그리는 메서드
    public void draw(Graphics2D g) {
        for (int i = 0; i < map.length; i++) {
            for (int j = 0; j < map[0].length; j++) {
                if (map[i][j] > 0) {
                    // 벽돌이 존재할 경우 그리기
                    g.setColor(Color.white);
                    g.fillRect(j * brickWidth + 80, i * brickHeight + 50, brickWidth, brickHeight);

                    // 벽돌 테두리 그리기
                    g.setStroke(new BasicStroke(3));  // 벽돌 테두리의 두께 설정
                    g.setColor(Color.black);  // 벽돌의 테두리를 검은색으로 설정
                    g.drawRect(j * brickWidth + 80, i * brickHeight + 50, brickWidth, brickHeight);
                }
            }
        }
    }

    // 벽돌의 값을 업데이트하는 메서드
    public void setBrickValue(int value, int row, int col) {
        map[row][col] = value;  // 벽돌의 상태 값을 변경 (0이면 제거된 상태)
    }
}
