package skiplist
====

    import "github.com/hydra13142/container/skiplist"

TYPES

	type SkipList struct {
		// contains filtered or unexported fields
	}

跳表类型

	func New() *SkipList

创建一个跳表

	func (this *SkipList) Len() int

返回跳表长度

	func (this *SkipList) Reset()

清空重置跳表

	func (this *SkipList) Insert(n int64, s string, v interface{}) bool

插入跳表新的值，如已存在相同键的值，不作修改并返回假

	func (this *SkipList) InsertUpdate(n int64, s string, v interface{})

如该键不存在值则插入新值，如已存在则更新旧值

	func (this *SkipList) Delete(n int64, s string) bool

删除跳表已有的值，如该键不存在值，返回假

	func (this *SkipList) DeleteByIndex(n int) bool

删除跳表第n个值

	func (this *SkipList) Search(n int64, s string) *Element

从跳表中搜索，int64和string的参数为键

	func (this *SkipList) SearchByIndex(n int) *Element

返回跳表中第n个值（下标从0开始）

	type Element struct {
		// contains filtered or unexported fields
	}

代表一个元素

	func (this *Element) Next() bool

向后遍历

	func (this *Element) Prev() bool

向前遍历

	func (this *Element) Key() (int64, string)

返回当前元素的键

	func (this *Element) Val() interface{}

返回当前元素的值

	func (this *Element) Set(v interface{})

设置当前元素的值
