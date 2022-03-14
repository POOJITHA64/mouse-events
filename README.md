# mouse-events
import java.awt.*;
import java.applet.*;
import java.awt.event.*;
/*<applet code="mouse_events" width=100 height=100>
</applet>*/
public class mouse_events extends Applet implements MouseListener,MouseMotionListener
{
	String msg=" ";
	int mouseX=0,mouseY=0;
	public void init()
	{
		addMouseListener(this);
		addMouseMotionListener(this);
	}
	public void mouseClicked(MouseEvent me)
	{
		mouseX=me.getX();
		mouseY=me.getY();
		msg="mouse clicked";
		repaint();
	}
	public void mouseEntered(MouseEvent me)
	{
		mouseX=me.getX();
		mouseY=me.getY();
		msg="mouse entered";
		repaint();
	}
	public void mouseExited(MouseEvent me)
	{
		mouseX=me.getX();
		mouseY=me.getY();
		msg="mouse exited";
		repaint();
	}
	public void mousePressed(MouseEvent me)
	{
		mouseX=me.getX();
		mouseY=me.getY();
		msg="mouse pressed";
		repaint();
	}
	public void mouseReleased(MouseEvent me)
	{
		mouseX=me.getX();
		mouseY=me.getY();
		msg="mouse released";
		repaint();
	}
	public void mouseDragged(MouseEvent me)
	{
		mouseX=me.getX();
		mouseY=me.getY();
		msg="*";
		showStatus("dragging mouse at"+mouseX+","+mouseY);
		repaint();
	}
	public void mouseMoved(MouseEvent me)
	{
		showStatus("mousing mouse at"+me.getX()+","+me.getY());
	}
	public void paint(Graphics g)
	{
		setBackground(Color.red);
		setForeground(Color.yellow);
		g.drawString(msg,mouseX,mouseY);
	}
}
