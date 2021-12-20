# ApplicationContextWare     implement     Aware

## 何希望被通知它运行的ApplicationContext对象要实现的接口。

ResourceLoaderAware   ApplicationEventPublisherAware

例如，当一个对象需要访问一组协作 bean 时，实现这个接口是有意义的。 请注意，通过 bean 引用进行配置比仅出于 bean 查找目的实现此接口更可取。
如果对象需要访问文件资源，即想要调用getResource ，想要发布应用程序事件，或者需要访问 MessageSource，也可以实现此接口。 但是，在这种特定场景中，最好实现更具体的ResourceLoaderAware 、 ApplicationEventPublisherAware或MessageSourceAware接口。
请注意，文件资源依赖项也可以作为org.springframework.core.io.Resource类型的 bean 属性公开，通过字符串填充，并由 bean 工厂进行自动类型转换。 这消除了为了访问特定文件资源而实现任何回调接口的需要。
org.springframework.context.support.ApplicationObjectSupport是应用程序对象的一个方便的基类，实现了这个接口。

# ServletContext

Web 服务器在 servlet 初始化时提供该 servlet



# ContextLoaderListener.contextInitialized

tomcat监听器，tomcat启动时将spring初始化Root上下文： XmlWebApplicationContext