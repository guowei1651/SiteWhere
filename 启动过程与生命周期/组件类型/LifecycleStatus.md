**LifecycleStatus**:
```java
public enum LifecycleStatus {

	/** Component is stopped */
	Stopped,

	/** Component is starting */
	Starting,

	/** Component is started */
	Started,

	/** Component is pausing */
	Pausing,

	/** Component is paused */
	Paused,

	/** Component is stopping */
	Stopping,

	/** Component startup failed with an error */
	Error;
}
```