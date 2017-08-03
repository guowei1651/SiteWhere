**LifecycleComponent**：(sitewhere-core:com.sitewhere.server.lifecycle)
这个类比较长这里只摘录几个比较重要的方法。
```java
	public void lifecycleStart() {
		LifecycleStatus old = getLifecycleStatus();
		setLifecycleStatus(LifecycleStatus.Starting);
		getLogger().info(getComponentName() + " state transitioned to STARTING.");
		try {
			if (old != LifecycleStatus.Paused) {
				start();
			}
			setLifecycleStatus(LifecycleStatus.Started);
			getLogger().info(getComponentName() + " state transitioned to STARTED.");
		} catch (SiteWhereException e) {
			setLifecycleStatus(LifecycleStatus.Error);
			setLifecycleError(e);
			getLogger().error(getComponentName() + " state transitioned to ERROR.", e);
		} catch (Throwable t) {
			setLifecycleStatus(LifecycleStatus.Error);
			setLifecycleError(new SiteWhereException(t));
			getLogger().error(getComponentName() + " state transitioned to ERROR.", t);
		}
	}

	public void lifecycleStop() {
		setLifecycleStatus(LifecycleStatus.Stopping);
		getLogger().info(getComponentName() + " state transitioned to STOPPING.");
		try {
			stop();
			setLifecycleStatus(LifecycleStatus.Stopped);
			getLogger().info(getComponentName() + " state transitioned to STOPPED.");
		} catch (SiteWhereException e) {
			setLifecycleStatus(LifecycleStatus.Error);
			setLifecycleError(e);
			getLogger().error(getComponentName() + " state transitioned to ERROR.", e);
		} catch (Throwable t) {
			setLifecycleStatus(LifecycleStatus.Error);
			setLifecycleError(new SiteWhereException(t));
			getLogger().error(getComponentName() + " state transitioned to ERROR.", t);
		}
	}
```