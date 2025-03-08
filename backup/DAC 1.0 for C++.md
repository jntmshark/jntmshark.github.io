闲着无聊，研究了一个“库”——DAC；它的主要功能就是一个类似json库，的一个库吧。。。
> [!TIP]
> 现在就只开发了一点点...（如下）
```cpp
#include <bits/stdc++.h>
#define DAC_VERSION "1.0 for C++"
using namespace std;
namespace dac {
	struct dac_c {
		string DACFile;
		string Key;
	};
	class dac_t {
		dac_c& dacc;
	public:
		dac_t(dac_c& TDACC) : dacc(TDACC) {}
	};
}
```
##### 它的用法会在1.0版本正式编写完成之后详细介绍ヾ(^▽^*)))