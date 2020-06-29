# Save-Data-Shared-Pref..-Android

```java
public class SaveData {
    public static final String PREFERENCES = "AEROPAQ_SAVE_DATA";

    // Getters
    private static SharedPreferences getPreferences(Context ctx) {
        return ctx.getSharedPreferences(PREFERENCES, 0);
    }

    public static String getString(Context ctx, String key) {
        SharedPreferences prefs = getPreferences(ctx);
        return prefs.getString(key, "");
    }

    public static int getInt(Context ctx, String key) {
        SharedPreferences prefs = getPreferences(ctx);
        return prefs.getInt(key, 0);
    }

    public static long getLong(Context ctx, String key) {
        SharedPreferences prefs = getPreferences(ctx);
        return prefs.getLong(key, 0L);
    }

    public static boolean getBoolean(Context ctx, String key) {
        SharedPreferences prefs = getPreferences(ctx);
        return prefs.getBoolean(key, false);
    }

    public static float getFloat(Context ctx, String key) {
        SharedPreferences prefs = getPreferences(ctx);
        return prefs.getFloat(key, 0f);
    }

    // Setters

    public static void putString(Context ctx, String key, String value) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.putString(key, value).apply();
    }

    public static void putBoolean(Context ctx, String key, boolean value) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.putBoolean(key, value).apply();
    }

    public static void putLong(Context ctx, String key, long value) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.putLong(key, value).apply();
    }

    public static void putInt(Context ctx, String key, int value) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.putInt(key, value).apply();
    }

    public static void putFloat(Context ctx, String key, float value) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.putFloat(key, value).apply();
    }

    public static void remove(Context ctx, String key) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.remove(key).apply();
    }

    public static void clear(Context ctx) {
        SharedPreferences.Editor editor = getPreferences(ctx).edit();
        editor.clear().apply();
    }
}
```
