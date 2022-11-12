# RESUME ROUTINE LOAD

## 功能

恢复已暂停 routine load 导入任务，通过 [PASUE](../data-manipulation/PAUSE%20ROUTINE%20LOAD.md) 命令可以暂停导入的任务，并进行 routine load 任务属性的修改，详细操作请参考 [alter routine load](../data-manipulation/alter-routine-load.md)。

## 语法  
```sql
    RESUME ROUTINE LOAD FOR job_name;
```
## 参数  
| **参数** | **必选** | **说明**                     |
| :------- | :------- | :--------------------------- |
| job_name  | 是       | 待手动刷新的物化视图的名称。 |

## 示例
恢复名称为 test1 的例行导入作业。

```sql
    RESUME ROUTINE LOAD FOR test1;
```
