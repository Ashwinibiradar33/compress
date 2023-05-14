import javax.swing.*;
import java.awt.*;
import java.util.List;
import java.util.ArrayList;
import javax.swing.*;


public class INTERFACE extends JFrame {
    private int[][] maze = {{1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1},
            {1, 0, 1, 0, 1, 0, 1, 0, 0, 0, 0, 0, 1},
            {1, 0, 1, 0, 0, 0, 1, 0, 1, 1, 1, 0, 1},
            {1, 0, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 1},
            {1, 0, 0, 1, 0, 0, 0, 0, 1, 1, 1, 0, 1},
            {1, 0, 1, 0, 1, 1, 1, 0, 1, 0, 0, 0, 1},
            {1, 0, 1, 0, 1, 0, 0, 0, 1, 1, 1, 0, 1},
            {1, 0, 1, 0, 1, 1, 1, 0, 1, 0, 1, 0, 1},
            {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 9, 1},
            {1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1}};
    JLabel label;
    public List<Integer> path = new ArrayList<>();
    public INTERFACE() {

        setTitle ("Maze Solver");
        getContentPane().setBackground(Color.LIGHT_GRAY);
        getContentPane().setLayout(null);
        setVisible(true);
        //label=new JLabel("Maze Solver");
        setSize(1000,720);
        setForeground(Color.WHITE);
        //setBackground(Color.LIGHT_GRAY);
        setFont(new Font("DIALOG",Font.ITALIC,19));
        //this.add(label);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        DFS.searchpath(maze,1,1,path);
        System.out.println(path);


    }
    @Override
    public void paint(Graphics g){
        g.translate(50,50);
        for(int i=0;i<maze.length;i++){
            for(int j=0;j<maze[0].length;j++){
                Color color;
                switch (maze[i][j]){
                    case 1:color=Color.DARK_GRAY;break;
                    case 9:color=Color.RED;break;
                    default:color=Color.WHITE;break;

                }
                g.setColor(color);
                g.fillRect(30*j,30*i,30,30);
                g.setColor(Color.RED);
                g.drawRect(30*j,30*i,30,30);

            }
        }
        for(int i=0;i<path.size();i+=2){
            int path_x=path.get(i);
            int path_y=path.get(i+1);
            System.out.println("X coordinates"+path_x);
            System.out.println("Y coordinates"+path_y);
            g.setColor(Color.GREEN);
            g.fillRect(30*path_x,30*path_y,15,15);
        }
    }
    public static void main(String[] args){
        INTERFACE view=new INTERFACE();
        view.setVisible(true);

    }

}
