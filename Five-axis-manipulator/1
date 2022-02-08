/*
	编译时间：2022.2.8
	适用主板：Arduino nano
	食用方法：把舵机端口自行修改
	适用机型：五轴(180°舵机)机械臂
	舵机端口：底部		 3
			  第一关节   5
			  第二关节	 6
			  第三关节	 9
			  夹子		 10
*/

#include <Servo.h>

//定义舵机名
Servo lowest;
Servo joint1;
Servo joint2;
Servo joint3;
Servo clip;

//舵机端口 (只修改最后的数字)
//可使用端口: 3 5 6 9 10 11
#define lowest_PIN 3  //底部舵机  (0°--180°)
#define joint1_PIN 5  //第一关节  (0°--180°)
#define joint2_PIN 6  //第二关节  (0°--180°)
#define joint3_PIN 9  //第三关节  (0°--180°)
#define clip_PIN 10   //夹持舵机  (0°--150°)

//舵机角度读取变量
int read_1 = 0;
int read_2 = 0;
int read_3 = 0;
int read_4 = 0;
int read_5 = 0;

void reset()
{
	lowest.write(90);
	joint1.write(90);
	joint2.write(90);
	joint3.write(90);
	clip.write(90);
	delay(250);
	write_lowest(0);
	write_joint1(0);
	write_joint2(0);
	write_joint3(0);
	write_clip(0);
}

void write_lowest(int a)
{
	read_1 = lowest.read();
	if (read_1 > a) {
		for (read_1;read_1 > a;read_1--)
		{
			lowest.write(read_1);
			delay(30);
		}
	}
	else if (read_1 = a) {

	}
	else if (read_1 < a) {
		for (read_1;read_1 < a;read_1++)
		{
			lowest.write(read_1);
			delay(30);
		}
	}
}

void write_joint1(int b)
{
	read_2 = joint1.read();
	if (read_2 > b) {
		for (read_2;read_2 > b;read_2--)
		{
			joint1.write(read_2);
			delay(30);
		}
	}
	else if (read_2 = b) {

	}
	else if (read_2 < b) {
		for (read_2;read_2 < b;read_2++)
		{
			joint1.write(read_2);
			delay(30);
		}
	}
}

void write_joint2(int c)
{
	read_3 = joint2.read();
	if (read_3 > c) {
		for (read_3;read_3 > c;read_3--)
		{
			joint2.write(read_3);
			delay(30);
		}
	}
	else if (read_3 = c) {

	}
	else if (read_3 < c) {
		for (read_3;read_3 < c;read_3++)
		{
			joint2.write(read_3);
			delay(30);
		}
	}
}

void write_joint3(int d)
{
	read_4 = joint3.read();
	if (read_4 > d) {
		for (read_4;read_4 > d;read_4--)
		{
			joint3.write(read_4);
			delay(30);
		}
	}
	else if (read_4 = d) {

	}
	else if (read_4 < d) {
		for (read_4;read_4 < d;read_4++)
		{
			joint3.write(read_4);
			delay(30);
		}
	}
}

void write_clip(int e)
{
	read_5 = clip.read();
	if (read_5 > e) {
		for (read_5;read_5 > e;read_5--)
		{
			clip.write(read_5);
			delay(30);
		}
	}
	else if (read_5 = e) {

	}
	else if (read_5 < e) {
		for (read_5;read_5 < e;read_5++)
		{
			clip.write(read_5);
			delay(30);
		}
	}
}


void setup()
{
	//初始化各个舵机名对应的舵机端口
	lowest.attach(lowest_PIN);
	joint1.attach(joint1_PIN);
	joint2.attach(joint2_PIN);
	joint3.attach(joint3_PIN);
	clip.attach(clip_PIN);
	Serial.begin(9600);  //串口频率设为9600
	reset();  //重置舵机角度
}


void loop()
{
	/*	编写格式
	*	write_lowest(角度);		底部
	*	write_joint1(角度);		第一关节
	*	write_joint2(角度);		第二关节
	*	write_joint3(角度);		第三关节
	*	write_clip(角度);		夹子
	*/
}