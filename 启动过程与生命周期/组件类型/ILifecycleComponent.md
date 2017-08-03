**ILifecycleComponent**:

```java
public interface ILifecycleComponent {

	/**
	 * Get the unique component id.
	 * 
	 * @return
	 */
	public String getComponentId();

	/**
	 * Get human-readable name shown for component.
	 * 
	 * @return
	 */
	public String getComponentName();

	/**
	 * Get component type.
	 * 
	 * @return
	 */
	public LifecycleComponentType getComponentType();

	/**
	 * Get current lifecycle status.
	 * 
	 * @return
	 */
	public LifecycleStatus getLifecycleStatus();

	/**
	 * Gets the last lifecycle error that occurred.
	 * 
	 * @return
	 */
	public SiteWhereException getLifecycleError();

	/**
	 * Get the list of contained {@link ILifecycleComponent} elements.
	 * 
	 * @return
	 */
	public List<ILifecycleComponent> getLifecycleComponents();

	/**
	 * Starts the component while keeping up with lifecycle information.
	 */
	public void lifecycleStart();

	/**
	 * Start the component.
	 * 
	 * @throws SiteWhereException
	 */
	public void start() throws SiteWhereException;

	/**
	 * Pauses the component while keeping up with lifecycle information.
	 */
	public void lifecyclePause();

	/**
	 * Indicates to framework whether component can be paused.
	 * 
	 * @return
	 * @throws SiteWhereException
	 */
	public boolean canPause() throws SiteWhereException;

	/**
	 * Pause the component.
	 * 
	 * @throws SiteWhereException
	 */
	public void pause() throws SiteWhereException;

	/**
	 * Stops the component while keeping up with lifecycle information.
	 */
	public void lifecycleStop();

	/**
	 * Stop the component.
	 * 
	 * @throws SiteWhereException
	 */
	public void stop() throws SiteWhereException;

	/**
	 * Find components (including this component and nested components) that are of the
	 * given type.
	 * 
	 * @param type
	 * @return
	 * @throws SiteWhereException
	 */
	public List<ILifecycleComponent> findComponentsOfType(LifecycleComponentType type)
			throws SiteWhereException;

	/**
	 * Get component logger.
	 * 
	 * @return
	 */
	public Logger getLogger();

	/**
	 * Logs the state of this component and all nested components.
	 */
	public void logState();
}
```