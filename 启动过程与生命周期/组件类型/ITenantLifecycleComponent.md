**ITenantLifecycleComponent**:

```java
public interface ITenantLifecycleComponent extends ILifecycleComponent {

	/**
	 * Set tenant for component.
	 * 
	 * @param tenant
	 */
	public void setTenant(ITenant tenant);

	/**
	 * Get tenant for component.
	 * 
	 * @return
	 */
	public ITenant getTenant();
}
```