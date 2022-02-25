# SqliteDataBaseSample
Quickly create routines to remind yourself what you should be doing and when. Basically this application is for sqlite database. Designed for ANDROID.



final CookieSyncManager cookieSyncManager = CookieSyncManager.createInstance(this);
    final CookieManager cookieManager = CookieManager.getInstance();
    cookieManager.removeAllCookie();
    cookieManager.setAcceptCookie(true);
    String[] cookies = getCookie(cookieManager, "https://myaccount.ee.co.uk/login-dispatch/?fa=register");
    for (String cookie : cookies) {
        cookieManager.setCookie("https://myaccount.ee.co.uk/login-dispatch/?fa=register", cookie);
    }
    cookieSyncManager.sync();
    webView.loadUrl("https://myaccount.ee.co.uk/login-dispatch/?fa=register");
    
    public String[] getCookie(CookieManager cookieManager, String siteName){
        String cookies = cookieManager.getCookie(siteName);
        String[] cookiesArray=cookies.split(";");
        return cookiesArray;
    }
