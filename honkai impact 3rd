/*******************************************************************************************************
	1》获取窗口句柄，得到窗口坐标
	2》由窗口坐标计算相对坐标
	3》截图，遍历取得关键坐标值
		图像灰度处理，计算哈希值，并与之匹配
	4》模拟键鼠操作，操控模拟器实现对应功能
	5》检测玩家角色，自动设置出战队伍，并自动运行对应战斗数据
	6》有条件添加一个窗口实现用户交互

	1》使用循环，判断
	2》调用win32API，图像处理库EasyX
	3》匹配图片可使用哈希值
*******************************************************************************************************/


#include <graphics.h>
#include <conio.h>
#include <WinUser.h>
#include <Windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#pragma comment (lib, "User32.lib")
#define random(x) (rand()%x)

#define ckbl 0.915072


void Sakura(void)
{
	int i,j;
		for (i = 0; i < 999999; i++)
		{
			j = 0;
			if(j<75)
			{
				keybd_event(74, 0, 0, 0);
				keybd_event(74, 0, KEYEVENTF_KEYUP, 0);
				srand((int)time(0));
				j = random(150);
				printf("%d", j);
				Sleep(j);
			}
			
		}
	
}

void Bronya(void)
{

}

void Rozaliya(void)
{
	int i, j;
	for (i = 0; i < 999999; i++)
	{
		j = 0;
		if (j < 75)
		{
			keybd_event(74, 0, 0, 0);
			keybd_event(74, 0, KEYEVENTF_KEYUP, 0);
			srand((int)time(0));
			j = random(150);
			printf("%d", j);
			Sleep(j);
		}

	}
}

int main()
{
	int  wdl, wdt, wdr, wdb;														//定义窗口四点坐标

	RECT rect;																		//定义矩形值
	HWND hwnd = FindWindow(L"Qt5QWindowIcon", L"崩坏3 - MuMu模拟器");				//获得窗口句柄
	GetWindowRect(hwnd, &rect);														//获得MuMu模拟器的四点坐标
	printf("%d\t%d\t%d\t%d\n", rect.left, rect.top, rect.right, rect.bottom);			//输出四点坐标
	printf("%#x", hwnd);
	//窗口xy坐标赋值
	wdl = rect.left;
	wdt = rect.top;
	wdr = rect.right;
	wdb = rect.bottom;

	//计算各键位相对坐标值
	int exggx,exggy;
	exggx = ckbl * (wdr - wdl) + wdl;
	exggy = ckbl * (wdb - wdt) + wdt;
	//因为发现拿到的坐标值不匹配，目前正在计算相关数据，求公式中~
	//数据计算较耗时，先写后面的程序
	//使用vs管理员开启，否则无法正常运行


	Rozaliya();
	

	::SetCursorPos(1439,812);
	mouse_event(MOUSEEVENTF_LEFTDOWN | MOUSEEVENTF_LEFTUP, 0, 0, 0, 0);

}
