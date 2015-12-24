#Share Your PHPStorm Live Templates
Abbreviation Description

> Template

###**Forms**
Seeing Jeffrey using variations of these to quickly create forms was what first made me realise how much time could be saved using templates. These are integrated to work well with the Twitter Bootstrap framework.

**fo** Form open tag

    {!! Form::open() !!}
**fc** Form close tag

    {!! Form::close() !!}
**textfield** Text form field

    <!--- $VALUE$ Field --->
    <div class="form-group">
        {!! Form::label('$NAME$', '$VALUE$:') !!}
        {!! Form::text('$NAME$', null, ['class' => 'form-control']) !!}
    </div>
**emailfield** Email form field

    <!--- $VALUE$ Field --->
    <div class="form-group">
        {!! Form::label('$NAME$', '$VALUE$:') !!}
        {!! Form::email('$NAME$', null, ['class' => 'form-control']) !!}
    </div>
**passwordfield** Password form field

    <!--- $VALUE$ Field --->
    <div class="form-group">
        {!! Form::label('$NAME$', '$VALUE$:') !!}
        {!! Form::password('$NAME$', ['class' => 'form-control']) !!}
    </div>
**textareafield** Text area form field

    <!--- $VALUE$ Field --->
    <div class="form-group">
        {!! Form::label('$NAME$', '$VALUE$:') !!}
        {!! Form::textarea('$NAME$', null, ['class' => 'form-control']) !!}
    </div>
**hiddenfield** Hidden form field

    {!! Form::hidden('$NAME$', $VALUE$) !!}
**submitfield** Submit form field

    <!--- $VALUE$ Field --->
    <div class="form-group">
        {!! Form::submit('$NAME$', ['class' => 'btn btn-primary']) !!}
    </div>
**req** Require field (add in the attribute array of any form field type to make field required.

    'required' => 'required'
###**Annotations**
I've been playing with 5.0 for a few weeks now and so I've added a few route annotation templates. I'm sure more will be added over the coming months.

**anno** Add docblock ready for annotations below

    /**
    * $ANNOTATIONS$
    * @return Response
    */
**@G** Get route annotation

    @Get("$ROUTE$", as="$NAME$")
**@P** Post route annotation

    @Post("$ROUTE$", as="$NAME$")
**@M** Get route annotation

    @Middleware("$NAME$")
###**Blade Live Templates**
I’ve been using these less since native blade support was added to PHPStorm but they are still useful.

**@ex** Blade extend

    @extends('$VIEW$')
**@fe** Blade foreach

    @foreach($GROUP$ as $INDIVIDUAL$)
        $ACTION$
    @endforeach
**@if** Blade if

    @if($BOOLEAN$)
        $OPERATION$
    @endif
**@ife** Blade if/else

    @if($BOOLEAN$)
        $OPERATION$
    @else
    
    @endif
**@inc** Blade include

    @include('$INCLUDE$')
**@sect** Blade section

    @section('$SECTION$')
        $CONTENT$
    @endsection
**@yi** Blade yield

    @yield('$YIELD$')
**bb** {{ }} unescaped blade tags

    {{ $CODE$ }}
**bbb** {!! !!} escaped blade tags

    {!! $CODE$ !!}
**view** New view from layout

    @extends('$LAYOUT$')
    
    @section('content')
        $CONTENT$
    @stop
###**Testing**
A few testing templates, I’m only just getting properly into test so I will be adding to these.

**cci** Codeception $I->

    $I->$FUNCTION$
**@test** Test outline

    /** @test */
    public function it_$METHOD$()
    {
        // Given
            $GIVEN$
        // When
            $WHEN$
        // Then
            $THEN$
     }
 

###**HTML**
I use these when I'm working on a throw away project and need to quickly import some basic styles and scripts.

**bootcss** Bootstrap css CDN link

    <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css"/>
**bootjs** Bootstrap js CDN link

    <script src="//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js"></script>
**jquery** jQuery CDN link

    <script src="//ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
**lorem** lorem ipsum generator

    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
###**Misc**
A few more that don’t quite fit into any category

**lt** Link to

    {!! link_to('$PATH$', '$TEXT$') !!}
**ltr** Link to route

    {!! link_to_route('$ROUTE$', '$TEXT$') !!}
**errors** Error loop

    @if($errors->any())
        <ul>
    @foreach($errors->all() as $error)
        <li>{{ $error }}</li>
    @endforeach
        </ul>
    @endif

References [link](https://laracasts.com/discuss/channels/tips/share-your-phpstorm-live-templates)