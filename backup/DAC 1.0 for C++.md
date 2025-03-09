闲着无聊，研究了一个“库”——DAC；它的主要功能就是一个类似json库，的一个库吧。。。
> [!TIP]
> 现在就只开发了一点点...（如下）
```cpp
#include <bits/stdc++.h>
#include<windows.h>
#define DAC_VERSION "1.0 for C++"
using namespace std;
namespace dac {
	struct dac_c {
		string DACFile;
		string Key;
	};
	class dac_t {
		dac_c& dacc;
		unordered_map<string, string> dat;
		UINT MESSAGEEXT(string ext) {
			if (ext == "Error") {
				return MB_OK | MB_ICONERROR;
			} else if (ext == "Info") {
				return MB_OK | MB_ICONASTERISK;
			} else if (ext == "EXCLAMATION") {
				return MB_OK | MB_ICONEXCLAMATION;
			} else {
				return MB_OK | MB_ICONEXCLAMATION;
			}
		}
		void ERR(string ext, string err) {
			string message = "[" + ext + "]: " + err;
			MessageBoxA(NULL, message.c_str(), "", MESSAGEEXT(ext));
		}
	public:
		dac_t(dac_c& TDACC) : dacc(TDACC) {}
	};
}
```
##### 它的用法会在1.0版本正式编写完成之后详细介绍ヾ(^▽^*)))