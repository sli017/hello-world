# hello-world
//sli017 for studying
//master edit 1
package Socket;

import java.net.*;
import java.io.*;

public class TestUDPServer
{
	public static void main(String args[]) throws Exception
	{
		byte buf[] = new byte[1024];
		DatagramPacket dp = new DatagramPacket(buf, buf.length);
		DatagramSocket ds = new DatagramSocket(5678);
		while(true)
		{
			ds.receive(dp);
			System.out.println(new String(buf,0,dp.getLength()));
			//ByteArrayInputStream bais = new ByteArrayInputStream(buf);
			//DataInputStream dis = new DataInputStream(bais);
			//System.out.println(dis.readLong());
		}
	}
}

